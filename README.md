# eBooks & Notes Companion App

An offline-first, highly customizable Android application that turns reading and note-taking into an active learning experience. With fully local processing, cloud and local AI integration, smart study metrics, and hands-free text-to-speech (TTS), this app serves as your ultimate study dashboard and reader.

Be a tester of pre-release app, email: android.xapps-lab@gmail.com
Link: https://play.google.com/store/apps/details?id=com.xappslab.enotebookcompanion

---

## 📸 Screenshots

### Installation

<table>
  <tr>
    <td align="center"><img src="screenshots/APK_Install-1.jpg" width="220"/><br/><sub>Step 1 – Download & Install</sub></td>
    <td align="center"><img src="screenshots/APK_Install-2.jpg" width="220"/><br/><sub>Step 2 – Open Installer</sub></td>
    <td align="center"><img src="screenshots/APK_Install-3.jpg" width="220"/><br/><sub>Step 3 – Allow Installation</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="screenshots/APK_Install-4.jpg" width="220"/><br/><sub>Step 4 – Complete Install</sub></td>
    <td align="center"><img src="screenshots/APK_Install-5A_DataPath&Permision.jpg" width="220"/><br/><sub>Step 5A – Set Data Path</sub></td>
    <td align="center"><img src="screenshots/APK_Install-5B_DataPath&Permision.jpg" width="220"/><br/><sub>Step 5B – Grant Permissions</sub></td>
  </tr>
</table>

### PDF Library & Reading

<table>
  <tr>
    <td align="center"><img src="screenshots/ebooksLibrary.png" width="220"/><br/><sub>eBooks Library</sub></td>
    <td align="center"><img src="screenshots/ebooksLibrary_ContentsOfCategory.png" width="220"/><br/><sub>Category Contents</sub></td>
    <td align="center"><img src="screenshots/ReadingDashboard.png" width="220"/><br/><sub>Reading Dashboard</sub></td>
  </tr>
</table>

### Study Playlists & Organization

<table>
  <tr>
    <td align="center"><img src="screenshots/CreateReadingList.png" width="220"/><br/><sub>Create Playlist</sub></td>
    <td align="center"><img src="screenshots/addtoReadingLists.png" width="220"/><br/><sub>Add to Playlist</sub></td>
    <td align="center"><img src="screenshots/configure_ebooksPath.png" width="220"/><br/><sub>Configure Workspace Path</sub></td>
  </tr>
</table>

### Text-to-Speech (TTS)

<table>
  <tr>
    <td align="center"><img src="screenshots/TTS_ReadingOnGoing.png" width="220"/><br/><sub>TTS Reading in Progress</sub></td>
    <td align="center"><img src="screenshots/Trigger_TTS.png" width="220"/><br/><sub>Trigger TTS</sub></td>
    <td align="center"><img src="screenshots/TTS_mode.png" width="220"/><br/><sub>TTS Mode Settings</sub></td>
  </tr>
</table>

### Markdown Notes & Study Dashboard

<table>
  <tr>
    <td align="center"><img src="screenshots/createANote.png" width="220"/><br/><sub>Create a Note</sub></td>
    <td align="center"><img src="screenshots/markDownNotes.png" width="220"/><br/><sub>Markdown Notes View</sub></td>
    <td align="center"><img src="screenshots/dashboard.png" width="220"/><br/><sub>Study Dashboard</sub></td>
  </tr>
</table>

### AI Quiz Generation

<table>
  <tr>
    <td align="center"><img src="screenshots/quizLists.png" width="220"/><br/><sub>Quiz Lists</sub></td>
    <td align="center"><img src="screenshots/quiz_Question&Answers.png" width="220"/><br/><sub>Quiz Q&A</sub></td>
    <td align="center"><img src="screenshots/quize_generate1.png" width="220"/><br/><sub>Generate Quiz – Step 1</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="screenshots/quize_generate2_save.png" width="220"/><br/><sub>Generate Quiz – Step 2</sub></td>
    <td align="center"><img src="screenshots/quize_generate3_save.png" width="220"/><br/><sub>Generate Quiz – Step 3</sub></td>
    <td align="center"><img src="screenshots/quize_generate4_Questions&Answers.png" width="220"/><br/><sub>Generated Q&A</sub></td>
  </tr>
</table>

### Settings, Goals & About

<table>
  <tr>
    <td align="center"><img src="screenshots/readinggoals.png" width="220"/><br/><sub>Reading Goals</sub></td>
    <td align="center"><img src="screenshots/llm_cloud&localprovider.png" width="220"/><br/><sub>AI Provider Settings</sub></td>
    <td align="center"><img src="screenshots/test-timer & appThem.png" width="220"/><br/><sub>Timer & App Theme</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="screenshots/aboutUS.png" width="220"/><br/><sub>About</sub></td>
    <td></td>
    <td></td>
  </tr>
</table>

---

## 🚀 Core Features

- **Local PDF Reader**: View books, save page progress, highlight text, and link selections to related notes.
- **Markdown Note Manager**: Create, edit, and organize Markdown notes. Quickly append summaries or key takeaways from PDFs.
- **Study Playlists**: Group related books into custom playlists to organize your reading curriculum.
- **AI-Powered Learning (Dual Engines)**:
  - **Cloud AI (API)**: Connect to a cloud AI provider for fast, state-of-the-art responses via API key.
  - **LM Studio Server**: Run open-source LLMs fully local on your own network with auto-model detection.
- **Text-to-Speech (TTS)**: Listen to your books with custom voices, speaking rates, and pitches. The app prevents your screen from dimming/sleeping while TTS is active.
- **Dashboard & Gamified Metrics**:
  - Weekly and daily goals for pages read and minutes studied.
  - Daily completion percentages shown on study playlists and quizzes.
  - Interactive activity calendar mapping your study intensity.
- **Database Portability & Auto-Backup**: Restores your reading history, notes, and quiz metrics automatically across app upgrades or package changes.

---

## 📂 Workspace Folder Setup & Database Structure

All content is managed through a single **Workspace Directory** selected using Android's Storage Access Framework (SAF). The app scans, organizes, and writes all files directly inside this folder.

To set up your workspace:
1. Create a folder in your external storage (e.g., `eNotesBooksWorkspace`).
2. Select this folder in the App settings under **Workspace Folder**.
3. The app will automatically initialize the following subdirectories:
   - `eBooks/` — Place your PDF files here. Group them into subfolders (e.g., `eBooks/ComputerScience/`, `eBooks/History/`) and the app automatically displays them as categories.
   - `eNotes/` — Houses all your Markdown notes (`.md`).
   - `eQuiz/` — Stores AI-generated Markdown quiz files, nested by category.
   - `backups/` — Used by the app to auto-save the SQLite database copy.

---

## 💾 Database Portability, Backup & Restore

To ensure you never lose your progress, highlights, playlist structures, and study statistics, the application supports both automatic and manual database migrations:

### 1. Automatic Workspace Backup & Restore
- **Backup**: Every time the app scans or syncs your workspace (on startup or manual refresh), it flushes all Write-Ahead Log (WAL) entries and copies the SQLite database to `backups/enotesbooks_backup.db` within your workspace folder.
- **Restore**: On a fresh install or package migration (e.g., moving to `com.xappslab.enotebookcompanion`), selecting the same workspace folder detects the backup and automatically restores all your progress.

### 2. Manual Export & Import
- In the **Settings Screen**, scroll to the **Database Management** section:
  - **Export DB**: Launches a document picker to save a copy of your database anywhere (e.g., cloud drives, SD cards).
  - **Import DB**: Import a previously exported database file to recover your notes, highlights, and history.

---

## 🤖 AI Configuration

To start generating summaries, questions, or custom study guides, configure one of the supported AI providers in Settings.

### 1. Cloud AI Provider (API-Based)
- **Get an API Key**: Obtain an API key from your preferred cloud AI provider.
- **Setup**:
  - Input your API key in Settings.
  - Select your preferred model from the available options.
- **Security**: The API key is stored locally in Android Encrypted SharedPreferences and is **never** shared externally.

### 2. LM Studio Server (100% Offline Local AI)
- **Run the Server**: Run [LM Studio](https://lmstudio.ai/) on a PC connected to the same Wi-Fi network. Load a model (e.g., Llama 3, Phi-3, Mistral) and enable the Local Server.
- **Setup**:
  - In Settings, input the LM Studio Server URL (e.g., `http://192.168.1.100:1234`).
  - Click **Detect Models** to fetch currently loaded models from the server.
  - Choose your model from the dropdown.

---

## 🛠️ Building & Deployment

Package namespace: `com.xappslab.enotebookcompanion`

### Prerequisites
- JDK 17
- Android SDK 36 (minSdk 24)

### Building
```powershell
# Set Java Home to Android Studio's JBR
$env:JAVA_HOME="C:\Program Files\Android\Android Studio\jbr"

# Run unit tests
.\gradlew.bat test

# Build Play Store bundle (AAB)
.\gradlew.bat bundleRelease

# Build unsigned release APK
.\gradlew.bat assembleRelease
```

---

## 📋 Release Notes

### v2.01
- Fix: Grid Heatmap not updating
- Fix: Gemini API Key Validation Confirmation
- Fix: LM Studio Server Link

---

## ℹ️ About

| | |
|---|---|
| **App Name** | eBooks & Notes Companion App |
| **Version** | 2.01 |
| **Developer** | xAPPS-Lab.ca |
| **Website** | [androidapps.xapps-lab.com](https://androidapps.xapps-lab.com) |
| **LinkedIn** | [jstaguan](https://www.linkedin.com/in/jstaguan) |
