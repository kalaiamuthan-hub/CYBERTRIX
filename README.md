# CYBERTRIX // Capture The Flag (CTF) Cybersecurity Platform

> **"Think. Exploit. Capture The Flag."**  
> Edition: CYBERTRIX CTF 2026

CYBERTRIX is a premium, futuristic cybersecurity competition platform designed for college-level and professional CTF tournaments. Built with cutting-edge cyber aesthetics, real-time Firestore database synchronization, role-based authentication, dynamic challenge administration, and zero-compromise security architecture.

---

## 🚀 Key Highlights & Features

### 1. Cyber Interface & Visual Aesthetics
- **Dark Theme with Cyber Accents**: Deep cyber black background (`#03060d`), neon cyan (`#00f3ff`), electric blue, purple accents (`#bd00ff`), and alert red.
- **Glassmorphism & Glowing Borders**: Futuristic semi-transparent cards with backdrop blur and pulsing cyber accents.
- **Interactive Cyber Canvas**: Live constellation particles responding to mouse parallax and cursor proximity.
- **Synthesized Web Audio Engine**: Zero-asset retro-cyber audio synthesizers for boot sequences, button clicks, and "ACCESS GRANTED" / "ACCESS DENIED" chimes (with sound mute toggle).
- **Scanline & CRT Micro-Effects**: Subtle cyber grid perspective and scanline overlay.
- **Animated Terminal Boot Sequence**: Hacker-style boot logs upon platform initialization.

### 2. Participant Arena Experience
- **Authentication**: Email & password clearance with Firestore user profiles (`users/{uid}`).
- **Participant Dashboard**: Real-time stats, total points, challenges solved, current rank, animated progress bar, solved challenges breakdown, and recent submission logs.
- **Challenge Arena**:
  - Filter by category: **WEB, CRYPTO, FORENSICS, OSINT, REVERSE ENGINEERING, MISC**.
  - Filter by difficulty: **EASY, MEDIUM, HARD**.
  - Real-time search by challenge name or keywords.
  - Interactive challenge detail modal with simulated clues, raw artifacts, accordion hints, and standard flag submission field (`CYBERTRIX{...}`).
  - Duplicate submission prevention and instant score updates.
- **Live Leaderboard**:
  - Ranked by highest score with tie-breaker logic (highest solves count and earliest submission timestamp).
  - Cyber podium for Top 3 operatives with custom gold, silver, and bronze crowns.
  - Automatic highlighting of current authenticated player.
  - Live Firestore data synchronization across public, dashboard, and admin views.
- **Public Announcement System**:
  - Real-time broadcasts from the administrative center.
  - Important alert badges with pulsing glow effect.

### 3. Hidden Administrative Control Center
- **Hidden Access Shortcut**: Press `CTRL + SHIFT + A` on any desktop page to open the restricted Admin Terminal modal.
- **Role-Based Authorization**: Protected by Firestore security checks (`users/{uid}.role === 'admin'`).
- **Control Center Overview**: Live telemetry, total players, active players, challenges count, total submissions, total solves, points awarded, and live UTC clock.
- **Dynamic Challenge Management**:
  - Add, edit, delete, and re-point challenges dynamically without code edits.
  - Status management: `ACTIVE`, `LOCKED` (visible but blocked), or `HIDDEN`.
  - Instant propagation to the public arena via Firestore listeners.
- **Announcement Control**: Create, edit, publish/unpublish, and mark urgent announcements.
- **Player Management**: Inspect competitor dossiers, view solved challenges, and audit submission attempts.
- **Submission Audit Log**: Real-time telemetry feed of all incoming flags with Correct/Incorrect and challenge filters.
- **Event Control**: Toggle event status (`UPCOMING`, `LIVE`, `ENDED`), manage countdown timestamps, and toggle open/closed registration.

---

## 📂 Project Structure

```
CRYPTX/
├── index.html                  # Main Landing Page with hero, boot terminal, & live broadcasts
├── login.html                  # Participant Authentication Portal
├── register.html               # New Operative Enrollment
├── dashboard.html              # Participant Dashboard & Telemetry
├── challenges.html             # Challenge Arena with filters & modals
├── challenge.html              # Standalone Challenge View
├── leaderboard.html            # Public Live Standings & Podium
├── rules.html                  # Rules of Engagement & Code of Conduct
├── firestore.rules             # Production Firebase Security Rules
│
├── admin/                      # Restricted Administrative Sector
│   ├── index.html              # Admin Authentication Gateway
│   ├── dashboard.html          # Admin Control Center & Telemetry
│   ├── players.html            # Operative Dossiers & Solves Inspector
│   ├── challenges.html         # Dynamic Challenge Management (CRUD)
│   ├── submissions.html        # Real-time Submission Audit Log
│   ├── leaderboard.html        # Synchronized Admin Standings
│   ├── announcements.html      # Broadcast Management & Controls
│   └── settings.html           # Event Lifecycle & Firebase Config
│
├── css/
│   ├── style.css               # Core theme, cyber tokens, glassmorphism, & animations
│   ├── dashboard.css           # Challenge cards, leaderboard podium, & progress bars
│   └── admin.css               # Admin layout, glowing sidebar, & audit tables
│
├── js/
│   ├── firebase-config.js      # Firebase credentials configuration
│   ├── firebase.js             # Dual-engine Firestore & Auth provider
│   ├── auth.js                 # Authentication logic & session state
│   ├── challenges.js           # Challenge arena rendering & flag submissions
│   ├── leaderboard.js          # Standings calculations & podium rankings
│   ├── submissions.js          # Participant telemetry & submission tracking
│   ├── announcements.js        # Public broadcast feed with real-time sync
│   ├── admin.js                # Privileged administrative operations
│   ├── event.js                # Event countdown timer & status sync
│   ├── sound.js                # Web Audio API cyber synthesizer
│   └── background.js           # Interactive canvas particles & admin shortcut listener
│
└── assets/
    ├── logo/                   # Vector branding assets
    └── icons/                  # Favicons and symbols
```

---

## 🔑 Pre-Configured Credentials

### Administrative Root Account
- **Access Route**: `CTRL + SHIFT + A` on any public page, or navigate to `/admin/index.html`
- **Email**: `admin@cybertrix.ctf`
- **Password**: `CyberAdmin#2026`
- **Role**: `admin`

### Sample Competitor Operatives
All seeded players use the default password: `password123`
- `wolf@cybertrix.ctf` (Codename: `CyberWolf` - 850 PTS)
- `nullbyte@cybertrix.ctf` (Codename: `NullByte` - 700 PTS)
- `shadow@cybertrix.ctf` (Codename: `ShadowRoot` - 650 PTS)

---

## 🏁 Pre-Seeded CTF Challenges & Flags

| Challenge | Category | Level | Pts | Solution Flag |
| :--- | :--- | :--- | :--- | :--- |
| **Hidden Gateway** | Web | Easy | 100 | `CYBERTRIX{h1dd3n_h34d3r_byp4ss}` |
| **Cookie Maze** | Web | Medium | 200 | `CYBERTRIX{c00k13_m0nst3r_s3ss10n}` |
| **Broken Cipher** | Crypto | Easy | 100 | `CYBERTRIX{c43s4r_rot13_d3c0d3d}` |
| **RSA Lock** | Crypto | Hard | 300 | `CYBERTRIX{sm4ll_pr1m3s_f4ct0r_br34k}` |
| **Digital Footprint**| Forensics | Easy | 100 | `CYBERTRIX{3x1f_m3t4d4t4_tr4c3r}` |
| **Memory Leak** | Forensics | Medium | 200 | `CYBERTRIX{m3m0ry_dum9_str1ngs_f0und}` |
| **Trace The Shadow** | OSINT | Easy | 100 | `CYBERTRIX{g30_c00rd1n4t3s_tr4ck3d}` |
| **Crack The Binary** | Reverse | Hard | 300 | `CYBERTRIX{x0r_k3y_r3v3rs3_3ng1n33r}` |
| **Cyber Puzzle** | Misc | Medium | 150 | `CYBERTRIX{mult1_l4y3r_b4s364_h3x}` |
| **SQLi Bastion** | Web | Hard | 250 | `CYBERTRIX{sqli_un10n_s3l3ct_pwn}` |

*(New challenges can be dynamically created at runtime from the Admin Panel).*

---

## ⚡ Running Locally

You can run CYBERTRIX using any standard static HTTP server:

```powershell
# Option 1: Python HTTP Server
python -m http.server 3000

# Option 2: Node.js npx serve
npx -y serve -p 3000 .
```

Open your browser at `http://localhost:3000`.

---

## 🔒 Firebase Integration & Security Rules

CYBERTRIX includes a dual-engine database layer:
1. **Local Cyber-MockStore with BroadcastChannel**: Out of the box, all pages and tabs synchronize state in real time without any setup required.
2. **Production Firebase Cloud**: To connect to your live Firebase project, paste your configuration credentials in `js/firebase-config.js` or via `Admin Dashboard -> Event Control -> Configure Firebase Keys`.

Deploy the provided `firestore.rules` to your Firebase project:
```bash
firebase deploy --only firestore:rules
```

---

© 2026 CYBERTRIX. All Rights Reserved. Designed for cybersecurity excellence.
