<div align="center">
  <img src="logo.webp" width="120" height="120" alt="Qatra Logo" style="border-radius: 24px; box-shadow: 0 12px 40px rgba(0, 229, 255, 0.3);" />
  
  # 🩸 Qatra (قطرة)
  ### The Ultimate Health-Tech & Social Solidarity Super App for Morocco. 🕊️🇲🇦
  
  [![License: MIT](https://img.shields.io/badge/License-MIT-CCFF00.svg)](https://opensource.org/licenses/MIT)
  [![Platform: Web & Android](https://img.shields.io/badge/Platform-Web%20%26%20Android-00E5FF.svg)](#)
  [![Firebase: Active](https://img.shields.io/badge/Firebase-Realtime%20Database-FFCA28.svg)](https://firebase.google.com/)
  
  **"Connecting hearts, mobilizing care, and saving lives in real-time."**
</div>

---

## 🌟 Overview

**Qatra** is a state-of-the-art, multi-faceted Super App engineered to revolutionize blood donation and decentralized healthcare logistics in Morocco. Built from the ground up to address real-world medical challenges, Qatra bridges the gap between donors, patients, certified healthcare professionals, pharmacies, and clinics.

By pairing a futuristic, high-performance web dashboard with a Kotlin-powered mobile app, Qatra ensures emergency blood requests find donors in minutes, and patients receive critical home nursing, physical therapy, and medical supplies instantly.

---

## 🚀 Key Features & Modules

### 1. 🩸 Blood Donation Command Center
* **Live SOS Broadcasts**: Doctors and clinics can initiate urgent geo-targeted SOS alerts.
* **Haversine Distance Matching**: A high-efficiency Kotlin algorithm parses active donor coordinates to alert only those within a 10km radius of the hospital, preventing message fatigue.
* **Gamified Loyalty System**: Donors earn points, digital badges (`منقذ النخبة` ✨, `درع الوطن` 🛡️, `سفير الحياة` 💎), and track their lifetime lives-saved contribution.
* **Digital QR Passport**: Enables instant, secure donor check-in at centers.

### 2. 🩺 Home Healthcare Concierge (طبيبك القريب)
* **On-Demand Home Services**: Patients can request certified home care, including wound care (`💉 تمريض وتضميد الجروح`) and physiotherapy (`🧘 الترويض الطبي`).
* **360° Real-Time Provider Radar**: Licensed nurses and physiotherapists utilize a radar simulator screen to view pending local requests on a spatial map.
* **Secure Provider Wallets**: Providers receive direct payments, track their earnings, manage custom commission structures, and review transaction logs.
* **Administrative Verification (OTP)**: Strict credentials screening verified via WhatsApp and activated securely through generated OTP codes.

### 3. 🏪 Smart Pharmacy & Parapharmacy Hub (الصيدلية الذكية والبارافارماسي)
* **Strategic Partnerships**: Direct API & database integrations with licensed pharmacies and parapharmacies in major cities (**Rabat, Salé, Casablanca**), syncing live stock catalog, unit prices, and store locations.
* **Interactive Radar Search**: Enables patients and providers to scan nearby pharmacies on a map showing distances, real-time hours, and verified item availability.
* **The 4-Stage Care & Delivery Lifecycle (مراحل دورة حياة الطلب والتوصيل):**
  1. **Selection & Reservation (الاختيار والحجز)**: The patient selects needed medical items (e.g., dressings, sterile gauze, sanitizers, or monitors) from the partner pharmacy. The items are locked in the database and linked to the home care request.
  2. **Unified Dispatch (إرسال الطلب الموحد)**: The combined healthcare + items request is broadcast to verified nearby nurses and physical therapists (within a 10km radius).
  3. **Caregiver Acceptance & Pickup (القبول والمسار)**: The caregiver accepts the request, picks up the reserved items from the partner pharmacy during their transit, and delivers them directly to the patient's home to perform the service.
  4. **DABA App Failover Integration (آلية الربط الاحتياطي مع تطبيق دابا)**: If the caregiver rejects the delivery portion, the Qatra engine instantly triggers an HTTP PUT request to the **DABA App database** (`https://daba-caregiver-default-rtdb.firebaseio.com/rejected_deliveries/`). This dispatch triggers a nearby DABA delivery ambassador ("Safir") to deliver the items, ensuring they arrive synchronously with the caregiver.

### 4. 💬 Anwar AI Chat Companion (المساعد الذكي "أنوار")
* **Generative AI Diagnostics**: Integrates an advanced conversational agent capable of communicating fluently in **Moroccan Darija** and Standard Arabic.
* **Educational & Guidance Agent**: Answers FAQs about blood donation eligibility, debunks myths, guides users on donation center hours, and offers psychological comfort to patients.

### 5. 💊 Peer-to-Peer Medication Solidarity (صيدلية التضامن)
* **Social Medicine Redistribution**: A secure, verified market for citizens to donate unexpired, surplus medications to low-income families.
* **Smart Search Filter**: Enables users to search by specific drug names or active ingredients within a local geographic radius to resolve temporary drug shortages.

### 6. 🏢 Hospital & Clinic Command Center (`clinic.html`)
* **SOS Broadcaster**: Allows medical staff to broadcast instant geo-targeted alerts to local donors of specific matching blood types in emergencies.
* **Digital Check-In Validator**: Generates unique OTP codes that validate successful blood donations when scanned/entered, updating the donor's digital blood passport instantly.
* **Stock & Donor Analytics**: Real-time visualization charts displaying donation rates, current reserves, and donor demographic insights.

### 7. ⚙️ Qatra Admin Concierge Console (`qatra_admin_concierge.html`)
* **Live Request Control Panel**: Monitor and manage all blood and healthcare requests.
* **Medical Certificate Inspection**: Dedicated verification column allowing admins to review medical certificates and publish/approve requests with a single click.
* **Interactive Notifications Drawer**: Built-in glassmorphic notifications drawer with real-time counters, audio alerts, and locally-synced read statuses.
* **Financial Ledger & Wallet Recharge**: Manage provider commission rates (15% to 20%), view transaction histories, and execute wallet recharges with detailed activity logging.

---

## 🛠️ Technology Stack

* **Mobile (Android)**: Kotlin, Jetpack Compose, Coroutines, Flow, Haptic Feedback, Google Play Location Services.
* **Web (Admin & Clinic)**: HTML5, CSS3 (Futuristic Dark Theme, HSL-color tokens, Glassmorphism), Vanilla JavaScript, Chart.js.
* **Backend & Database**: Firebase (Realtime Database, Authentication, Firestore, Hosting).
* **Cross-Platform Integration**: Direct REST API integration with the **DABA App** for delivery failover.

---

## 📂 Project Structure

```bash
├── 📱 app/                          # Kotlin Android Mobile App
│   ├── src/main/java/.../healthcare # Home Healthcare & Radar Compose Screens
│   └── src/main/java/.../repository # Safe Firebase Data Snapshot Parsers
├── 🏢 clinic.html                   # Medical Center Control Panel
├── 🌐 index.html                    # Main Portal & Donor Hub
├── ⚙️ qatra_admin_concierge.html     # High-End Admin Command Console
├── 📜 qatra_admin_concierge.js       # Real-time Admin Notifications & Actions
└── 📜 database.rules.json           # Secure RBAC Database Rules
```

---

## 💻 Getting Started

### Prerequisites
- Node.js & npm (for hosting/dev)
- Android Studio (for mobile development)

### Local Development
1. **Clone the repository**:
   ```bash
   git clone https://github.com/qatra-ma/qatra.git
   ```
2. **Setup Environment**:
   Create a `.env` file or database config file with your Firebase configuration.
3. **Run Web App**:
   ```bash
   npm install
   ```
4. **Deploy to Firebase**:
   ```bash
   firebase deploy
   ```

---

## 🔒 Security & Privacy

Qatra is built with a **Security-First** approach:
* **No-Index Protection**: Clinical and administrative dashboards contain non-indexing headers to prevent exposure to search engines.
* **Robust Deserialization**: Custom Kotlin parsers handle numeric database type casting safely, protecting the app from runtime crashes.
* **Role-Based Access Control**: Enforced rules in Firebase ensure patients, providers, and admins can only write/read authorized paths.

---

## 🤝 Partners & Integrations
* **Moroccan Pharmacy Syndicate**: Providing live pricing and product lists.
* **DABA App Ecosystem**: Direct integration with the DABA logistics network for medical delivery ambassador dispatch.

---

## 🌐 Connect With Us

Stay updated with the latest news and donor success stories:
* **Facebook**: [Qatra Official](https://web.facebook.com/profile.php?id=61589092855136)
* **Instagram**: [@qatra_ma](https://www.instagram.com/qatra_ma)
* **Official Website**: [qatra.web.app](https://qatra.web.app)

---

## 🤝 Contributors

* **Anouar BOUDEHBI** - Founder, Lead Developer & UI/UX Designer

---

<div align="center">
  <p>Qatra: Tech-Driven Wellness for Every Moroccan. 🕊️🇲🇦</p>
</div>
