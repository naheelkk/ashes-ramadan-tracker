🌙 Team Ashes | Ramadan Tracker

"Steadfast in faith, united in purpose."

A premium, multiplayer progressive web application designed to help Team Ashes track spiritual habits, Quran recitation, and fasting consistency during the holy month of Ramadan. Built with a "Privacy First" approach using Firebase Anonymous Authentication.

![WhatsApp Image 2026-02-15 at 4 33 29 PM](https://github.com/user-attachments/assets/13058276-4b2b-475d-b858-2f44db774166)


✨ Features

📊 Daily Accountability

Obligations: Track Fasting status, Charity (Sadaqah), and the 5 Daily Prayers.

Smart Scoring: Earn points for consistency to climb the team leaderboard.

Streak Logic: Intelligent streak calculation based on calendar dates.

📖 Quran Companion

Khatam Tracker: Visual progress bar for the 604 pages of the Quran.

Surah Logging: Select from all 114 Surahs or log specific pages.

Verification: "Trust but Verify" system—requires a written reflection if you read the translation to claim points.

🏆 Multiplayer Leaderboard

Real-time Updates: See team scores update instantly.

Live Rankings: Compete for the top spot in Fasting counts and Total Score.

Anonymous Profiles: No email/password required. Accounts are tied to the device.

📿 Spiritual Tools

Digital Tasbih: Integrated counter with haptic feedback.

Essential Duas: Library for Iftar, Suhoor, Ashras, and Laylatul Qadr.

Daily Verse: Rotating inspiring Quranic Ayahs.

🚀 Setup Guide

This app is a Single-File Application (SPA) powered by Firebase.

1. Prerequisite: Firebase

You need a free Firebase project to store the data.

Go to console.firebase.google.com.

Create a new project.

Enable Database: Build > Firestore Database > Create > Start in Test Mode.

Enable Auth: Build > Authentication > Sign-in method > Anonymous > Enable.

Get Config: Project Settings > General > Your Apps > Web (</>) > Register App.

Copy the firebaseConfig object.

2. Configure the App

Open index.html and look for lines ~30-40:

const firebaseConfig = {
    apiKey: "PASTE_YOUR_API_KEY",
    authDomain: "...",
    projectId: "...",
    // ... rest of your config
};


Paste your keys there.

3. Database Rules (Critical!)

To allow the app to write data, update your Firestore Rules in the Firebase Console:

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}


🌐 Deployment (GitHub Pages)

Create a new repository on GitHub.

Upload your index.html file.

Go to Settings > Pages.

Under Branch, select main and click Save.

Your app will be live at https://yourusername.github.io/repo-name/.

🎨 Customization

Logo: Search for <!-- LOGO PLACEHOLDER --> in the HTML to replace the flame icon with your own image <img>.

Colors: Modify the tailwind.config script at the top of the HTML file to change the Gold/Emerald/Ashes color scheme.

📄 License

This project is open-source. Feel free to modify it for your own team or community.
