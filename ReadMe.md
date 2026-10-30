# SetuExam (सेतु-परीक्षा)

> **National Candidate Clearinghouse for Higher Education Entrance Examinations**  
> *One Profile. One KYC. Universal Auto-Registry.*

---

## 📌 Problem Statement

Every year, millions of Indian Grade 12 and undergraduate aspirants apply for 6 to 12 distinct national and state entrance tests (e.g., JEE Main, BITSAT, VITEEE, UGEE, MET, COMEDK, NEET, CLAT). Conducting bodies (NTA, BITS Pilani, VIT, State CETs) operate isolated, legacy web portals that create acute friction:

* **Application Fatigue:** Candidates repeatedly enter identical biographical data, educational history, and academic scores across dozens of separate sites.
* **Incompatible Document Upload Specs:** Strict, conflicting photo and signature requirements lead to massive rejection rates (e.g., JEE requires 3.5×4.5 cm / 10KB–200KB JPEG; BITSAT requires 200×230 px / 50KB–100KB JPEG; COMEDK strictly caps files under 80KB). Students resort to unsafe third-party compression sites, exposing sensitive identification documents.
* **Date Clash Blind Spots:** Overlapping examination and slot windows across private universities and state bodies often go unnoticed until non-refundable fees are paid.
* **Narrow Application Windows:** Students frequently miss 7–10 day registration windows for secondary exams due to fragmented notification cycles and server outages.

---

## 💡 The Solution

**SetuExam** bridges this fragmentation into a single, high-trust civic portal built on the principle of **"One Profile. One KYC. Universal Auto-Registry."**

[Candidate KYC & Master Vault]
│
├───► In-Browser Canvas Transmuter (Auto-scales to 40KB/50KB/100KB specs)
│
├───► Multi-Exam Cart & Clash Detection (JEE, BITSAT, VITEEE, etc.)
│
├───► Auto-Register Queue & Mandates (Auto-submits when future portals open)
│
└───► Unified Master Timeline (Single Admit Card & Test Shift Calendar)


---

## 🚀 Key Features

### 1. Universal Cart & Stream Clearinghouse
* Browse and batch-select from 18+ accredited entrance exams across **Engineering**, **Medical & Allied**, **Management**, and **Law**.
* Dynamic fee calculation and single aggregated checkout via UPI / Net Banking.

### 2. Client-Side Document Transmuter Matrix (Zero AI Slop)
* **Single Master Upload:** Students upload high-resolution photographs and signatures once.
* **In-Browser Canvas Engine:** Runs client-side recursive binary search compression using HTML5 Canvas. If a portal requires under 40KB and an 80KB image is uploaded, it downscales and compresses in-memory without losing visual sharpness.
* **Privacy by Design:** Zero unencrypted photos or certificates are transmitted to external compression servers.

### 3. Date Clash Detection Engine
* Compares tentative and declared exam dates in real time.
* Displays proactive warning alerts for overlapping testing windows (e.g., *VITEEE (Apr 19–30) vs. MET Manipal (Apr 18–22)*) before payments are finalized.

### 4. Automated Launch Queue & Mandates
* For upcoming examinations whose registration portals have not yet opened (e.g., BITSAT or UGEE), candidates can queue their application in advance.
* Automatically dispatches application payloads and triggers pre-authorized RBI-compliant UPI AutoPay mandates the moment external portals go live—with zero upfront debits.

### 5. Unified Master Timeline
* Replaces scattered PDF public notices with a centralized, filterable calendar tracking:
  * Application submission status
  * City intimation slip announcements
  * Admit card downloads
  * Allocated exam shifts and test venue navigation

---

## 🛠️ Document Transmuter Compliance Matrix

| Examination | Target Dimensions | Target Format | Permitted Range | Output Size | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **JEE Main** | 350 × 450 px (3.5×4.5 cm) | JPEG | 10 KB – 200 KB | ~46 KB | ✅ Verified |
| **BITSAT** | 200 × 230 px | JPEG | 50 KB – 100 KB | ~74 KB | ✅ Verified |
| **VITEEE** | 300 × 400 px | PNG / JPEG | Max 300 KB | ~182 KB | ✅ Verified |
| **MET Manipal** | 200 × 200 px (1:1) | JPEG | 15 KB – 100 KB | ~58 KB | ✅ Verified |
| **COMEDK** | 300 × 400 px | JPEG | 20 KB – 80 KB | ~42 KB | ✅ Verified |

---

## 🎨 Civic-Tech Design System

* **No Decorative "AI Slop":** Zero floating 3D blobs, no neon gradients, and no glassmorphism overlays.
* **Color Palette:** High-trust institutional tones:
  * Primary Navy (`#071527` / `#0A1E38`)
  * Neutral Slate Borders (`#E2E8F0`)
  * Amber Alerts & Deadlines (`#D97706`)
  * Verified Emerald (`#15803D`)
* **Typography:** Plus Jakarta Sans & Inter for interface elements; JetBrains Mono for monetary figures, application IDs, and file brackets.

---

## 💻 Tech Stack

* **Frontend:** Modern HTML5, Tailwind CSS / Vanilla CSS, TypeScript / JavaScript
* **Image Processing:** HTML5 Offscreen `<canvas>` API with bicubic scaling & iterative quality compression
* **Storage:** LocalStorage for candidate state preservation and offline fallback
* **Testing:** Headless Chromium automation scripts (`verify-portal.cjs`)

---

## 🏁 Getting Started

### Prerequisites
* [Node.js](https://nodejs.org/) (v18.0.0 or higher)
* `npm` or `yarn`

### Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/](https://github.com/)<YOUR-USERNAME>/setuexam.git
Navigate to the project directory:

Bash
cd setuexam
Install dependencies:

Bash
npm install
Start the local development server:

Bash
npm run dev
Open http://localhost:5173 in your browser.

📂 Repository Structure
Plaintext
setuexam/
├── public/                 # Static assets, institutional emblems, and icons
├── src/
│   ├── components/         # Cart, stream selector, transmuter, and timeline
│   ├── data/
│   │   └── mockExams.json  # Comprehensive Indian entrance exam dataset
│   ├── utils/
│   │   └── canvasCompressor.js # In-browser iterative image compression engine
│   ├── App.jsx / App.ts    # Main view controller & dual-mode view switcher
│   └── main.jsx / index.js # Entry point
├── tests/
│   └── verify-portal.cjs   # Headless validation tests
├── package.json
└── README.md