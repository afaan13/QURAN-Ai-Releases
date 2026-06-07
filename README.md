# QURAN-AI — Premium Islamic Knowledge & Daily Companion

<p align="center">
  <img src="app/src/main/res/mipmap-xxxhdpi/ic_launcher_round.webp" width="120" alt="Noor App Icon"/>
</p>

<p align="center">
  <strong>Your intelligent Islamic companion — powered by AI, rooted in authentic scholarship.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white" alt="Android"/>
  <img src="https://img.shields.io/badge/Kotlin-2.1-7F52FF?logo=kotlin&logoColor=white" alt="Kotlin"/>
  <img src="https://img.shields.io/badge/Jetpack_Compose-UI-4285F4?logo=jetpackcompose&logoColor=white" alt="Compose"/>
  <img src="https://img.shields.io/badge/Firebase-Backend-FFCA28?logo=firebase&logoColor=black" alt="Firebase"/>
  <img src="https://img.shields.io/badge/Version-1.0.4-D4AF37" alt="Version"/>
</p>

---

## ✨ What is QURAN-AI?

QURAN-AI is a beautifully crafted, offline-capable Islamic assistant for Android. It combines AI-powered question answering with authentic Quranic scholarship, complete Tafseer coverage, multi-language translations, precision prayer times, and daily supplication reminders — all wrapped in a premium dark-emerald interface.

Whether you're looking for a quick answer about Islamic jurisprudence, reading Tafseer commentary, or need accurate prayer times without internet — NOOR has you covered.

---

## 📖 Islamic Knowledge Coverage

### Quran & Translations
- **Full 16-Line Mushaf** — Complete 604-page offline Quran reader optimized for edge-to-edge layout
- **Verse-Level Translation** — Accessible offline translation and search support
- **Urdu Translation** — Complete coverage for Urdu-speaking users
- **English Translation** — Accessible translations for English readers
- **Arabic Text** — Original Arabic scripture with Indo-Pak (Noorehuda) font styling

### Tafseer (Exegesis)
NOOR includes comprehensive Tafseer coverage from renowned scholars:
- **Bayaan-ul-Quran** — Maulana Ashraf Ali Thanvi (RA)
- **Tafheem-ul-Quran** — Syed Abul Ala Maududi (RA)
- **Ma'ariful Quran** — Mufti Muhammad Shafi (RA)
- **Tafseer Ibn Kathir** — Imam Ibn Kathir (RA)

### Hadith Collections
Authentic narrations sourced from the six major Hadith collections:
- Sahih Bukhari
- Sahih Muslim
- Sunan Abu Dawud
- Jami' at-Tirmidhi
- Sunan an-Nasa'i
- Sunan Ibn Majah

---

## 🚀 Key Features

### 📖 Offline Quran & Immersive Reader
- **16-Line Authentic Mushaf** — Optimized full-screen page images designed to feel like reading a physical Quran copy
- **Indo-Pak Calligraphic Font** — Tailored specifically for South Asian readers by utilizing the *Noorehuda* font style for Arabic titles and index listings
- **Edge-to-Edge Full Screen** — Renders behind transparent Android system bars, maximizing the size of page images to fill the screen
- **Floating Translucent HUD** — Clean, toggleable top overlays show current Surah, Juz, and Page numbers without cluttering the calligraphic area
- **Split Horizontal Search** — Double search inputs allow filtering by Surah Name/Number or executing direct page number jumps (clamped safely to pages 1..604 with complete error handling)
- **Background Downloader** — High-speed parallel downloader fetches all 604 page resources automatically upon launch with a dynamic factual UI that auto-advances to the app on completion

### 🤖 AI-Powered Islamic Q&A
- **Context-Aware Answers** — Ask any Islamic question and receive concise, authentic answers with inline scripture citations
- **Smart Citations** — Automatically appends clickable Quran verse and Hadith reference chips to every response
- **Multi-Turn Conversations** — Maintains context across follow-up questions within a session
- **Send on Enter** — Soft and hardware keyboard Enter key triggers immediate message sending instead of a newline
- **Concise by Default** — Responses are kept short and to the point; detailed explanations are provided only when you ask for them
- **RAG Architecture** — Retrieval-Augmented Generation ensures answers are grounded in authentic sources, not hallucinated

### 🔄 Resilient API Fallback Chain
The AI chat employs a robust 4-tier fallback system to ensure answers are always delivered:
1. **Cloud RAG Endpoint** — Primary retrieval via Firebase Cloud Functions
2. **Gemini API** — Direct client-side completions via Google's Gemini model
3. **OpenRouter API** — Secondary LLM fallback via OpenRouter
4. **Offline Cache** — Local Room database serves cached answers when fully offline

### 🕌 High-Precision Prayer Times (Offline)
- **Fully Offline Calculations** — No internet required; uses astronomical equations
- **GPS & Manual Location** — Auto-detect via GPS or enter coordinates manually
- **Multiple Calculation Methods** — Karachi, Muslim World League, ISNA, and more
- **Madhab Support** — Hanafi & Shafi'i Asr calculation rules
- **Daily Salah Notifications** — Exact alarm scheduling for each prayer time

### 🤲 Daily Dua Reminders
- **Curated Supplication Pool** — Verified duas categorized across daily slots (Pre-Fajr, Morning, Evening, etc.)
- **Smart Deduplication** — Never repeats the same dua within 7 consecutive notifications
- **Scheduled Alerts** — Precise alarm-based notifications via Android AlarmManager

### 📄 Export & Share
- **PDF Export** — Long-press any AI response to export it as a formatted PDF document
- **Share Instantly** — Share exported PDFs directly via any installed app

### ✏️ Chat Management
- **Edit Messages** — Tap the inline edit icon on any sent message to refine your question
- **Multi-Session Support** — Create, switch between, and delete conversation sessions from the side drawer
- **Session History** — All conversations are persisted locally and accessible anytime

### 🎨 Premium Design
- **Dark Emerald Theme** — Curated color palette with deep forest greens and golden accents
- **Animated Splash Screen** — Smooth scale & fade entrance with developer credit
- **Typewriter Effect** — AI responses stream word-by-word with optional haptic feedback
- **Smart Auto-Scroll** — Chat locks to bottom during streaming, dynamically handles long typing lists, pauses on manual scrolls, and automatically resumes when scrolled back to the bottom
- **Glassmorphic UI Elements** — Modern, polished interface elements throughout
- **Password reveal toggle** — Small eye icon allows toggling password text visibility in the Login/Signup screen
- **IME focus flow** — Soft keyboard transitions focus from Email field (Next action) straight into Password field, closing the keyboard (Done action) upon typing the password
- **Streamlined Onboarding** — Upgraded flow from 4 pages to 3 by removing the disclaimer warning screen so "Next" takes users directly to location permission options. Updated welcome title to "Welcome to Quran-Ai"

---

## 🛠️ Technology Stack

### Android Client
| Layer | Technology |
|---|---|
| **Language** | Kotlin 2.1 (JVM Target 17) |
| **UI Framework** | Jetpack Compose with Material 3 |
| **Architecture** | MVVM + Repository Pattern |
| **Dependency Injection** | Dagger Hilt 2.55 |
| **Local Database** | Android Room (SQLite) |
| **Preferences** | Jetpack DataStore |
| **Networking** | Retrofit 2.9 + OkHttp |
| **Serialization** | Kotlinx Serialization JSON |
| **Navigation** | Jetpack Navigation Compose |
| **Image Loading** | Coil Compose |
| **Markdown Rendering** | compose-markdown |
| **Prayer Calculations** | batoulapps/adhan |
| **Location** | Google Play Services Location |
| **Auth** | Firebase Auth + Google Sign-In |
| **Analytics** | Firebase Analytics |
| **Billing** | Google Play Billing Library |
| **Biometrics** | AndroidX Biometric |

### Backend
| Layer | Technology |
|---|---|
| **Runtime** | Node.js 20 (ES Modules) |
| **Functions** | Firebase Cloud Functions v5 |
| **Database** | Cloud Firestore |
| **Vector Search** | Pinecone |
| **AI Models** | Google Gemini, OpenRouter |
| **Auth** | Firebase Authentication |

---

## 📱 Requirements

- **Android 8.0+** (API 26)
- **Google Play Services** (for authentication & location)
- **Internet** (for AI chat; prayer times work fully offline)

---

## 🔒 Private Repository Notice

This repository contains the core codebase for **NOOR** and is kept strictly private. Public releases are published separately.

> **For developers**: Building locally requires your own API credentials in `local.properties` and a valid `google-services.json` in the `app/` directory.

---

<p align="center">
  Crafted with ❤️ by <a href="https://github.com/afaan13"><strong>AFAAN</strong></a>
</p>
