# PondChat — real-time browser chat

An original dark-themed chat app using HTML, CSS, JavaScript, Firebase Authentication, and Cloud Firestore.

## Included
- Email/password accounts
- Usernames
- Live group channels (`general`, `gaming`, `memes`)
- Direct messages by username
- Responsive layout for PC and phone

## Setup (Windows)

### 1) Make a Firebase project
1. Go to https://console.firebase.google.com/ and create a project.
2. Add a **Web app** from the project overview (`</>`).
3. Copy its Firebase configuration into `firebase-config.js`, replacing every `PASTE_...` placeholder.
4. Go to **Build → Authentication → Sign-in method** and enable **Email/Password**.
5. Go to **Build → Firestore Database** and create a database.
6. Open Firestore **Rules**, paste in the contents of `firestore.rules`, and click **Publish**.

Firebase's browser config is not a server password. Never put service-account keys or admin secrets in this folder.

### 2) Run locally
1. Install Node.js LTS from https://nodejs.org/ if needed.
2. Extract this folder somewhere easy, such as Desktop.
3. Open the `pondchat` folder in File Explorer.
4. Click the address bar, type `cmd`, press Enter.
5. Run `npx serve .` and accept the install prompt if shown.
6. Open the local URL printed in the terminal, often `http://localhost:3000`.

If Python is already installed, `python -m http.server 8000` also works; then visit `http://localhost:8000`.

### 3) Let friends use it
`localhost` is only your own computer. To chat from separate devices, deploy the files to a host you control using HTTPS, such as Firebase Hosting or GitHub Pages. All users must open the same URL and use accounts in the same Firebase project. A school network may block chat sites; follow school rules and do not try to bypass restrictions.

### Notes
- This is a starter project, not a fully moderated production chat service.
- Username and message content are visible to authenticated users in this project. Don't share personal details.
- Firebase rules restrict message creation to signed-in users and DM access to thread members, but the profile lookup is intentionally simple. For a public launch, add server-side username uniqueness, abuse reporting, rate limiting, blocking, and moderation.
