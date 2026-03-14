<p align="center">
  <img src="https://img.shields.io/badge/Status-In%20Development-yellow?style=for-the-badge" alt="Status"/>
  <img src="https://img.shields.io/badge/Hackathon-India%20Innovates%202026-blue?style=for-the-badge" alt="Hackathon"/>
  <img src="https://img.shields.io/badge/Domain-Digital%20Democracy-teal?style=for-the-badge" alt="Domain"/>
  <img src="https://img.shields.io/badge/Cost-%240%20Prototype-green?style=for-the-badge" alt="Cost"/>
</p>

# 🇮🇳 NagrikSeva — India's First AI-Powered Government Services Assistant

> **"NagrikSeva doesn't teach you the government process — it DOES the government process for you, in your language, on your phone, without a single bribe."**

NagrikSeva is an AI-powered omnichannel platform that delivers government services to every Indian citizen across **5 channels** — Mobile App, WhatsApp, SMS, Phone Call, and Web — in **all 22 scheduled Indian languages**. Built for the **India Innovates 2026** national hackathon (Digital Democracy domain).

---

## 🚨 Project Status

```
╔══════════════════════════════════════════════════════════════╗
║  🔬 IDEATION & ACTIVE DEVELOPMENT PHASE                     ║
║                                                              ║
║  ✅ Research & Problem Validation    — Complete               ║
║  ✅ System Architecture Design       — Complete               ║
║  ✅ Tech Stack Finalization          — Complete               ║
║  ✅ PPT Submission (8 slides)        — Submitted              ║
║  ✅ Project Report (25 pages)        — Complete               ║
║  ✅ FAQ Document (50 Q&A)            — Complete               ║
║  🔨 Backend API Development          — In Progress            ║
║  🔨 AI Model Integration             — In Progress            ║
║  ⏳ WhatsApp Bot Integration         — Upcoming               ║
║  ⏳ Flutter Mobile App               — Upcoming               ║
║  ⏳ Officer Dashboard (Next.js)      — Upcoming               ║
║  ⏳ IVR/SMS Channel Setup            — Upcoming               ║
╚══════════════════════════════════════════════════════════════╝
```

---

## 📋 Table of Contents

- [The Problem](#-the-problem)
- [Our Solution](#-our-solution)
- [How It Works](#-how-it-works)
- [Key Innovation](#-key-innovation-two-way-officer-citizen-bridge)
- [System Architecture](#-system-architecture)
- [Tech Stack](#-tech-stack)
- [Custom AI Models](#-custom-ai-models-not-just-apis)
- [Government API Integrations](#-government-api-integrations)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Documentation & Resources](#-documentation--resources)
- [Team](#-team)
- [Hackathon Details](#-hackathon-details)

---

## 😤 The Problem

India's 1.4 billion citizens interact with the world's largest bureaucracy through a broken system:

| The Reality | The Number | Source |
|---|---|---|
| Citizens who pay bribes for govt services | **39%** | Transparency International 2020 |
| India's Corruption Perceptions Index rank | **96th/180** (Score: 38/100) | CPI 2024 |
| Average bribe per household per year | **₹1,840** | TII-LocalCircles 2019 |
| Indians completely offline | **630 million** | IAMAI/Kantar 2024 |
| Rural internet penetration | **44.99%** | TRAI Q4 2024 |
| UMANG app actual active usage | **~20-25%** of registered users | Industry estimates |
| Ayushman Bharat utilization in rural areas | **1.3%** despite 67% awareness | NCBI/Cureus 2023 |
| PDS food grain leakage annually | **₹69,108 Crore** | ICRIER/IFPRI |
| Average office visits per govt service | **3-5 visits** | Field studies |

**The bottom line:** You can track a ₹200 Swiggy order in real-time, but you cannot track your own ₹60,000 pension application.

---

## 💡 Our Solution

NagrikSeva meets citizens **where they already are** — not where the government wants them to be.

### 5 Channels, One AI Brain

| Channel | Technology | Who It Serves |
|---|---|---|
| 📱 **Mobile App** | Flutter (Android + iOS) | Smartphone users |
| 💬 **WhatsApp** | Meta Cloud API | 500M+ Indian WhatsApp users |
| 📩 **SMS** | MSG91 (DLT compliant) | Feature phone users (₹500 phones) |
| 📞 **Phone Call** | Twilio IVR + Our STT/TTS | Illiterate citizens — just dial and talk |
| 🌐 **Web Portal** | Next.js 14 | Desktop users & government officers |

All 5 channels connect to the **same intelligent backend**. A citizen can start a query on WhatsApp and continue it on a phone call — full context is preserved.

### 4-Step Citizen Journey

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   01. DISCOVER   │────▶│   02. PREPARE    │────▶│    03. APPLY     │────▶│   04. TRACK      │
│                  │     │                  │     │                  │     │                  │
│ "मुझे birth     │     │ Documents needed │     │ AI scans docs,   │     │ Unique code:     │
│  certificate     │     │ Nearest office   │     │ pre-fills form,  │     │ NS-2026-XXXXX    │
│  banana hai"     │     │ Fees & timings   │     │ you confirm &    │     │ Real-time status │
│                  │     │ DigiLocker check │     │ submit           │     │ Officer bridge   │
└─────────────────┘     └─────────────────┘     └─────────────────┘     └─────────────────┘
```

---

## 🌟 Key Innovation: Two-Way Officer-Citizen Bridge

**No platform in India — not UMANG, not MyScheme, not any state portal — lets a government officer message a citizen directly about their application.**

NagrikSeva changes this:

```
                    speaks Telugu              translates to English
    ┌──────────┐  ──────────────▶  ┌──────────────┐  ──────────────▶  ┌──────────┐
    │ CITIZEN  │                    │ NagrikSeva   │                    │ OFFICER  │
    │          │  ◀──────────────  │     AI       │  ◀──────────────  │          │
    └──────────┘  receives Telugu   └──────────────┘  responds English  └──────────┘
```

- Officer types: *"Income certificate is from 2023, need one from last 6 months"*
- AI auto-translates to citizen's language (Telugu, Tamil, Bengali... any)
- Citizen receives on WhatsApp/SMS/Phone call
- Citizen responds in their language → auto-translated back for officer
- **Neither party needs to share a common language**

This converts every rejection into a **recoverable conversation**.

---

## 🏗 System Architecture

```
╔═══════════════════════════════════════════════════════════════════════════╗
║                          CITIZEN CHANNELS                                ║
║  📱 Flutter App  💬 WhatsApp  📩 SMS (MSG91)  📞 IVR (Twilio)  🌐 Web    ║
╠═══════════════════════════════════════════════════════════════════════════╣
║                       ▼ Unified API Gateway (FastAPI) ▼                  ║
╠═══════════════════════════════════════════════════════════════════════════╣
║                           AI ENGINE                                      ║
║  🎤 Custom Whisper STT    🔊 Custom VITS TTS    🧠 IndicBERT NLP        ║
║  👁 Gemini Flash Vision   🌍 Bhashini Translation                        ║
║                    ⭐ = Our Fine-Tuned Models                             ║
╠═══════════════════════════════╦═══════════════════════════════════════════╣
║       CORE SERVICES           ║         OFFICER DASHBOARD                ║
║  🔍 Scheme Matcher (700+)    ║  💬 Two-Way Messaging                    ║
║  📋 Document Scanner         ║  📊 Smart Priority Queue                 ║
║  📝 Smart Form Filler        ║  ⏱ SLA Monitoring                        ║
║  📊 Application Tracker      ║  📈 Analytics                            ║
║  ⚠️ Grievance Escalator      ║         ◀══════▶                          ║
║  📅 Life-Event Engine        ║    (Bidirectional Bridge)                 ║
╠═══════════════════════════════╩═══════════════════════════════════════════╣
║                        GOVERNMENT APIs                                   ║
║  🆔 Aadhaar eKYC   📂 DigiLocker   📊 data.gov.in   📝 CPGRAMS         ║
╠═══════════════════════════════════════════════════════════════════════════╣
║                    DATABASE & INFRASTRUCTURE                             ║
║  🐘 PostgreSQL     ⚡ Redis     ☁️ AWS S3     🐳 Docker     🔄 CI/CD     ║
╚═══════════════════════════════════════════════════════════════════════════╝
```

---

## 🛠 Tech Stack

### Frontend
| Technology | Purpose | Why This |
|---|---|---|
| **Flutter** | Mobile App (Android + iOS) | Native Indic script rendering, used by UIDAI for Aadhaar apps, AOT compilation for budget phones |
| **Next.js 14** | Web Portal + Officer Dashboard | SSR for fast load on slow connections, App Router, React Server Components |
| **Tailwind CSS** | UI Styling | Utility-first, consistent design system, rapid development |

### Backend
| Technology | Purpose | Why This |
|---|---|---|
| **FastAPI (Python)** | Core API Server | All AI/ML SDKs are Python-native, async by default, auto Swagger docs, 3x faster than Flask |
| **PostgreSQL** | Primary Database | JSONB for flexible scheme data, UTF-8 Indic support, ACID compliance for govt data |
| **Redis** | Cache + Real-time | Sub-ms caching, pub/sub for Socket.IO, session management, rate limiting |
| **Socket.IO** | Real-time Updates | Instant officer-citizen bridge messaging, live dashboard refresh |

### AI/ML — Our Custom Models ⭐
| Model | Purpose | Training Data |
|---|---|---|
| **Fine-tuned Whisper** | Speech-to-Text (10+ Indian languages) | IndicSUPERB/Kathbath (1,684 hrs, 12 languages) |
| **Fine-tuned VITS** | Text-to-Speech (natural Indian voices) | IndicTTS (13 languages) |
| **Fine-tuned IndicBERT** | Intent Classification (50+ govt intents) | AI4Bharat IndicBERT v2, 20.9B token corpus |
| **PaddleOCR (tuned)** | Offline Indic Document OCR | Curated Indian govt documents dataset |

### AI APIs
| API | Purpose |
|---|---|
| **Google Gemini Flash** | Reasoning LLM + Document Vision (1M token context, free tier) |
| **Bhashini (Govt of India)** | Translation engine — all 22 scheduled Indian languages |
| **Sarvam AI** | Backup STT/TTS, code-mixed language processing |

### Government Integrations
| API | Purpose |
|---|---|
| **Aadhaar eKYC** | Identity verification via sandbox.co.in |
| **DigiLocker** | Consent-based document fetch via Setu API |
| **data.gov.in + APISetu** | 4,200+ government APIs, scheme data |
| **CPGRAMS** | Automated grievance filing (92 ministries) |

### Communication
| API | Channel | Cost |
|---|---|---|
| **Meta WhatsApp Cloud API** | WhatsApp Bot | Free (1,000 service msgs/month) |
| **Twilio Voice** | Phone Call / IVR | $0.009/min India |
| **MSG91** | SMS Gateway | ₹0.15/SMS, DLT compliant |

### Infrastructure
| Technology | Purpose |
|---|---|
| **AWS Mumbai (ap-south-1)** | Cloud hosting — lowest India latency, free tier |
| **Docker** | Containerization — consistent deployment |
| **GitHub Actions** | CI/CD — automated testing and deployment |

> **Total Prototype Cost: $0** — Every service runs on free tiers.

---

## 🧠 Custom AI Models (Not Just APIs)

This is what separates NagrikSeva from every other hackathon project. **We don't just call APIs — we build our own models.**

### Why Custom?
- **Zero per-call cost** — models run on our servers
- **Domain-adapted** — trained on Indian government vocabulary
- **Code-mixing support** — handles "mera Aadhaar card update karna hai"
- **Offline capable** — PaddleOCR works without internet

### Model Pipeline
```
Voice Input → Whisper STT (our model) → IndicBERT (our model, 100ms) → Gemini Flash (reasoning)
           → Bhashini NMT (translation) → VITS TTS (our model) → Voice Output

Document  → PaddleOCR (our model) → Gemini Flash Vision (validation) → Form Pre-fill
```

80% of citizen messages are handled by IndicBERT alone (simple intent routing). Only complex queries reach Gemini Flash — keeping us within free tier limits.

---

## 🏛 Government API Integrations

| API | How We Use It | Access |
|---|---|---|
| **Aadhaar eKYC** | OTP-based identity verification | sandbox.co.in (10,000 free credits) |
| **DigiLocker** | Pull citizen documents with consent (DL, PAN, certificates) | Setu API (OAuth 2.0 flow) |
| **data.gov.in** | Scheme eligibility rules, office locations, statistics | REST API (1,000 req/hr) |
| **APISetu** | 4,200+ government APIs — MeeSeva, education, business | Sandbox available |
| **CPGRAMS** | Auto-draft and file grievances when SLA breached | Web integration (API planned) |
| **Bhashini** | ASR + NMT + TTS pipeline for 22 languages | Free for PoC |

---

## 📁 Project Structure

```
NagrikSeva/
├── README.md                    # You are here
├── backend/                     # FastAPI server (🔨 In Progress)
│   ├── app/
│   │   ├── main.py              # FastAPI app entry
│   │   ├── api/                 # API route handlers
│   │   │   ├── citizen.py       # Citizen-facing endpoints
│   │   │   ├── officer.py       # Officer dashboard endpoints
│   │   │   ├── schemes.py       # Scheme discovery & matching
│   │   │   └── documents.py     # Document upload & OCR
│   │   ├── core/                # Config, security, database
│   │   ├── models/              # SQLAlchemy/Pydantic models
│   │   ├── services/            # Business logic
│   │   │   ├── ai_engine.py     # AI model orchestration
│   │   │   ├── translation.py   # Bhashini/Sarvam integration
│   │   │   ├── ocr.py           # PaddleOCR processing
│   │   │   └── govt_apis.py     # Government API connectors
│   │   └── channels/            # Channel adapters
│   │       ├── whatsapp.py      # Meta Cloud API adapter
│   │       ├── sms.py           # MSG91 adapter
│   │       ├── ivr.py           # Twilio Voice adapter
│   │       └── websocket.py     # Socket.IO handler
│   ├── requirements.txt
│   └── Dockerfile
├── web/                         # Next.js officer dashboard (⏳ Upcoming)
├── mobile/                      # Flutter citizen app (⏳ Upcoming)
├── ai-models/                   # Model training scripts (⏳ Upcoming)
│   ├── whisper-finetune/
│   ├── vits-finetune/
│   ├── indicbert-finetune/
│   └── paddleocr-finetune/
├── docs/                        # Documentation
│   ├── architecture.png         # System architecture diagram
│   └── api-spec.yaml            # OpenAPI specification
├── docker-compose.yml
└── .github/
    └── workflows/
        └── ci.yml               # GitHub Actions CI/CD
```

---

## 🚀 Getting Started

> ⚠️ **Project is in active development.** Setup instructions will be updated as components are completed.

### Prerequisites
- Python 3.11+
- Node.js 18+
- Docker & Docker Compose
- PostgreSQL 15+
- Redis 7+

### Quick Start (Backend)
```bash
# Clone the repository
git clone https://github.com/vedant7007/Nagrik_seva.git
cd Nagrik_seva

# Set up Python environment
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys (Gemini, Bhashini, etc.)

# Run the server
uvicorn app.main:app --reload --port 8000
```

### Docker Setup
```bash
docker-compose up --build
```

### Environment Variables
```env
# AI APIs
GEMINI_API_KEY=your_gemini_key
BHASHINI_API_KEY=your_bhashini_key
SARVAM_API_KEY=your_sarvam_key

# Government APIs
AADHAAR_SANDBOX_KEY=your_sandbox_key
DIGILOCKER_CLIENT_ID=your_setu_client_id
DATA_GOV_API_KEY=your_datagov_key

# Communication
WHATSAPP_TOKEN=your_meta_token
TWILIO_ACCOUNT_SID=your_twilio_sid
MSG91_AUTH_KEY=your_msg91_key

# Database
DATABASE_URL=postgresql://user:pass@localhost:5432/nagrikseva
REDIS_URL=redis://localhost:6379

# AWS
AWS_ACCESS_KEY_ID=your_aws_key
AWS_SECRET_ACCESS_KEY=your_aws_secret
AWS_S3_BUCKET=nagrikseva-documents
```

---

## 📚 Documentation & Resources

| Document | Description | Link |
|---|---|---|
| 📄 **Project Report** | 25-page comprehensive report with research, architecture, tech deep-dive | [Google Drive](https://drive.google.com/) |
| ❓ **FAQ Document** | 50 judge Q&A covering technical, business, legal, and scalability questions | [Google Drive](https://drive.google.com/) |
| 🎬 **Demo Video** | Working prototype demonstration | Coming Soon |
| 📊 **PPT Submission** | 8-slide hackathon presentation | [Google Drive](https://drive.google.com/) |
| 🏗 **Architecture Diagram** | High-res system architecture infographic | [Google Drive](https://drive.google.com/) |

> 📂 **[Access Full Google Drive Folder →](https://drive.google.com/drive/folders/1ChA3DklA5Zh0l9stxMPwuQiK4ulZ0o2A?usp=sharing)** *(Contains all documentation, diagrams, demo video, and research)*

---

## 📊 Impact Projections

| Metric | Current Reality | With NagrikSeva |
|---|---|---|
| Citizens reachable | UMANG: 82M registered | **400M+** (WhatsApp + SMS + IVR) |
| Languages served | MyScheme: 2 | **22** (fine-tuned) |
| Office visits per service | 3-5 visits | **0-1 visits** |
| Bribery exposure | 39% pay bribes | **Near zero** (digital, no intermediary) |
| Application rejection rate | ~30-40% | **<10%** (AI pre-validation + bridge) |
| Cost per interaction | ₹250-500 | **₹2-5** |
| Estimated annual citizen savings | — | **₹15,000+ Crore** |

---

## 👥 Team

### SevaSquad — Vidya Jyothi Institute of Technology, Hyderabad

| Member | Role |
|---|---|
| **Vedant Manmath Idlgave** | Team Lead & Full-Stack Developer |
| **V Thanishka** | Frontend Developer (Flutter + Next.js) |
| **Devidi Ruthvik Reddy** | Backend Developer |
| **Sahithi Reddy** | Research & Documentation |
| **Saripella Anjana** | UI/UX Designer |
| **Nakka Abhinav** | Testing & DevOps |

---

## 🏆 Hackathon Details

| Detail | Info |
|---|---|
| **Event** | India Innovates 2026 |
| **Domain** | Digital Democracy |
| **Venue** | Bharat Mandapam, New Delhi |
| **Date** | March 28, 2026 |
| **Organizers** | HN x MCD, with DDU, IIT KGP, DTC, NSUT, GGSIPU |
| **Prize Pool** | ₹10,05,000 |

---

## 📜 License

This project is developed for the India Innovates 2026 hackathon. License details will be added upon project completion.

---

<p align="center">
  <i>"The measure of a democracy is not how many services it digitizes, but how many citizens it actually serves."</i>
  <br><br>
  <b>SevaSquad — VJIT, Hyderabad</b>
  <br>
  India Innovates 2026 🇮🇳
</p>
