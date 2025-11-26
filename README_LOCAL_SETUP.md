# Local Development Setup

## Running the App Locally

The app should be run using the Express server, NOT Live Server, to ensure proper Firebase and ES6 module support.

### Steps:

1. **Install dependencies** (if not already installed):
   ```bash
   npm install
   ```

2. **Start the Express server**:
   ```bash
   npm start
   ```
   Or for development with auto-reload:
   ```bash
   npm run dev
   ```

3. **Access the app**:
   - Open your browser and go to: `http://localhost:3000`
   - The app will automatically serve `daily-finance-tracker.html`

### Why not use Live Server (port 5501)?

- Live Server doesn't properly handle ES6 modules (Firebase SDK uses ES6 modules)
- CORS issues with Firebase services
- Missing proper MIME types for JavaScript modules
- The app is designed to work with Firebase hosting or a proper Express server

### Firebase Configuration

The app uses Firebase Firestore for data storage. Make sure:
- You have Firebase credentials configured in `daily-finance-tracker.html`
- Firebase project is set up and accessible
- Firestore rules allow read/write (check `firestore.rules`)

### Troubleshooting

If you see errors:
1. Make sure you're using `http://localhost:3000` (Express server), NOT port 5501
2. Check browser console for Firebase connection errors
3. Verify Firebase credentials are correct
4. Ensure Firestore rules allow your operations



