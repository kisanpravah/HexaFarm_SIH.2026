# 🌾 HexaFarm — KISAN PRAVAH

**Improving the Farmer Procurement Experience**

> **Anticipate · Orchestrate · Assure**

**KISAN PRAVAH** is an AI-enabled, multilingual procurement coordination platform that connects farmers and procurement centres — from crop planning all the way to payment.

Instead of reacting to farmers after they arrive at a centre, KISAN PRAVAH **forecasts demand before congestion occurs**. Farmers pre-register their crops, centres see expected arrivals and quantities in advance, and everyone gets clear, real-time visibility of queues, slots and payments.

| | |
|---|---|
| **Event** | Smart India Hackathon 2026 |
| **Problem Statement ID** | SIH26032 |
| **Theme** | Smart Automation |
| **PS Category** | Software |
| **Team Name** | HexaFarm |
| **Team ID** | 135883 |

---

## 🚜 Problem

Farmers often face long waiting times, a lack of information about procurement schedules, and uncertainty about procurement status. On the ground, this shows up as:

- No advance visibility of demand, so centres cannot plan capacity, staff, storage or weighing facilities
- Long queues and unnecessary physical waiting at centres
- Poor communication between farmers and procurement centres
- Uncertainty about where, when and at what rate to sell
- Little transparency in procurement progress and payment status
- Difficulty for low-literacy and non-smartphone users in accessing information

**Root causes of delay at procurement centres**

- Large seasonal arrival surges and uneven farmer arrival rates
- Insufficient or temporarily unavailable weighing machines
- Quality-testing and sampling queues, and shortage of testing staff
- Labour shortages for unloading, handling and loading
- Delays in bags/material availability
- Transportation and lifting delays after procurement
- Storage capacity constraints
- Manual or duplicate data entry and operational software issues
- Quality-standard disputes, retesting and review
- Weather and moisture-related quality and arrival disruptions
- Lack of real-time visibility for farmers and officials

---

## 💡 Our Solution

**KISAN PRAVAH** is an AI-enabled, multilingual procurement coordination platform that connects farmers and procurement centres — from crop planning to payment.

It is not just another token-booking application. It is an **intelligent procurement decision-support platform** that predicts bottlenecks, estimates waiting time, optimises farmer flow, and communicates with farmers through **WhatsApp or SMS** — even when smartphone access is limited.

The core idea is **Predict → Inform → Optimise → Notify**: the system does not merely report that a queue exists, it predicts how the queue will evolve and recommends an action.

**Key design principles**

- **No smartphone required** – smartphone users use WhatsApp and the web app; basic-phone users use two-way SMS. IVR, USSD and assisted kiosks are planned extensions.
- **One backend, many channels** – WhatsApp, SMS and the web app all use the same farmer database, centre database, queue engine and AI services.
- **Explainable AI** – predictions come with reasons (for example, which factor added how many minutes of delay).
- **Human in the loop** – centre-level actions recommended by the AI are approved by officials.
- **Data minimisation** – only the information needed for procurement services is collected.

---

## 🔄 How It Works — Process Flow

```
+----------------------------+
|          DECLARE           |
|      Crop + Quantity       |
+----------------------------+
               |
               v
+----------------------------+
|          PREDICT           |
|        AI Forecast         |
+----------------------------+
               |
               v
+----------------------------+
|          ALLOCATE          |
|       Centre + Slot        |
+----------------------------+
               |
               v
+----------------------------+
|           ARRIVE           |
|        Farmer Alert        |
+----------------------------+
               |
               v
+----------------------------+
|          PROCURE           |
|     Planned Processing     |
+----------------------------+
               |
               v
+----------------------------+
|           TRACK            |
|     Transaction Status     |
+----------------------------+
```

1. **Declare** – The farmer registers (OTP verification) and declares crop and quantity ahead of time.
2. **Predict** – The AI engine forecasts arrivals, quantities, waiting time, congestion and workload for each centre.
3. **Allocate** – The decision engine recommends a suitable centre and a lower-load slot, and issues a digital token.
4. **Arrive** – The farmer gets smart alerts (turn approaching, delays, slot reminders) and arrives around the suggested time instead of waiting at the centre.
5. **Procure** – The centre verifies documents and crop quality, weighs the produce and generates the bill.
6. **Track** – The farmer follows procurement status and payment until the money is credited.

### Farmer journey

1. Register – basic details and preferred procurement centre
2. Select crop and centre – view nearby centres and today's status
3. View and book slot
4. Receive digital token
5. Live queue tracking – queue position and farmers ahead
6. AI ETA prediction – waiting time from queue, speed, counters and historical data
7. Smart alerts – turn approaching, delay notifications, slot reminders
8. Arrive at centre around the suggested time
9. Verification and procurement – document and crop verification, quality check
10. Digital receipt – quantity, crop, rate, centre and date
11. Status tracking – procurement status and payment updates

### Procurement centre flow

1. Centre dashboard – today's schedule, live queue and slots
2. Token management – manage queue and call tokens
3. Quality check – moisture, foreign matter, broken grains
4. Weighing and entry – digital weighing and quantity record
5. Bill generation for the farmer
6. Upload bill and data to the government system
7. Government payment status – bill submitted → payment processing → payment credited → farmer notified

### Procurement status shown to the farmer

`Registered → Scheduled → Arrived → Testing → Weighing → Procured → Payment initiated`

---

## ✨ Key Features

### 👨‍🌾 Farmer (Mobile App / WhatsApp / SMS)
- Simple registration with minimal data: name, mobile number, village, district, language, crop, approximate quantity, preferred centre and communication preference
- Crop pre-registration (crop, quantity, expected date) before harvest
- **Smart centre recommendation** – based on distance, queue, predicted wait, capacity and crop eligibility, not distance alone
- **Smart slot recommendation** – suggests a lower-load time instead of only showing availability
- Slot booking and **digital token** linked to farmer, centre, appointment and crop/quantity
- **Live queue** – current token, farmers ahead, estimated wait and expected service time
- **AI waiting-time prediction**
- **Leave-and-return** – notified when the turn is approaching, so no unnecessary waiting at the centre
- Procurement status tracking, digital receipt and payment status
- WhatsApp and SMS alerts for booking, token, delay, approaching turn, rescheduling and status updates
- MSP, demand and weather insights to decide where and when to sell
- AI chatbot to answer questions and guide the farmer through the system
- Regional-language access: Marathi, Hindi and English (set per farmer)
- Mobile app screens: Login → Home → Crop Registration → Centre Recommendation → Slot Booking → Live Queue → Alerts → Quality → Receipt → Payment

**Example – WhatsApp**

> Farmer: Hi
> Bot: Choose 1 Book Slot, 2 My Token, 3 Queue Status, 4 Centre, 5 Procurement Status, 6 Payment.
> Bot: Token MH1542 | 11 farmers ahead | Estimated wait 34 minutes | Expected turn 11:40 AM.

**Example – SMS**

> Farmer sends: `STATUS 1542`
> System replies: `Token MH1542 | Ahead 11 | Wait 34 min | Reach around 11:20 AM.`

### 🏢 Procurement Centre (Web Dashboard)
- Live queues, station capacity, staff, storage, transport, bottlenecks, alerts and recommendations
- Expected arrivals and demand forecast for capacity planning
- Token management and calling the next farmer
- **Bottleneck detection** – identifies whether verification, testing, weighing, storage or transport is limiting throughput
- **What-if simulator** – simulate a machine failure, staff shortage, arrival surge or extra trucks and see the predicted effect
- **Mandi control room (digital-twin style view)** – Arrival → Verification → Quality Testing → Weighing → Procurement → Storage → Transport, with queue and capacity at every stage
- Reports and analytics, delay announcements

### 🛡️ Admin / Government Portal
- Real-time monitoring of demand, congestion and centre utilisation
- Procurement progress and payment visibility
- Role-based access for farmers, centre operators, district officers and administrators
- Audit trail for important procurement events

### 🌐 Accessibility & Inclusion
- Two-way SMS for basic-phone users; WhatsApp for smartphone users
- Multilingual messages (Marathi, Hindi, English)
- Future extensions: IVR, USSD and assisted kiosks

---

## 🏗️ System Architecture

```
+------------------------------------------------------------------------+
|                                 USERS                                  |
|                                                                        |
|  Farmers (WhatsApp / SMS / Web App)  |  Centre Operators  |  Officers  |
+------------------------------------------------------------------------+
                                     |
                                     v
+------------------------------------------------------------------------+
|                                FRONTEND                                |
|                                                                        |
|            Next.js + TypeScript + Tailwind CSS + shadcn/ui             |
| React Hook Form + Zod  |  Zustand  |  TanStack Query  |  Lucide Icons  |
+------------------------------------------------------------------------+
                                     ^
                                     |  REST / API calls
                                     v
+--------------------+    +--------------------+    +--------------------+
|   AUTHENTICATION   |    |   BACKEND / API    |    |      AI / ML       |
|                    |    |                    |    |                    |
|       Clerk        |    | Next.js API Routes |    |  Python + FastAPI  |
|(OTP for prototype) |<-->|      or Hono       |<-->|    scikit-learn    |
|                    |    |                    |    |OpenAI/Groq chatbot |
+--------------------+    +--------------------+    +--------------------+
                                     |
                                     |  read / write data, queue jobs
                                     v
+---------------+  +---------------+  +---------------+  +---------------+
|   PostgreSQL  |  |     Redis     |  |     BullMQ    |  |    pgvector   |
|  + Prisma ORM |  |   Live queue  |  |Background jobs|  |   (Optional)  |
|               |  |    + cache    |  |               |  |semantic search|
+---------------+  +---------------+  +---------------+  +---------------+
                                     |
                                     |  send alerts / store files
                                     v
+---------------+  +---------------+  +---------------+  +---------------+
|    WhatsApp   |  |  SMS Gateway  |  |   Amazon S3   |  |     Docker    |
|  Business API |  |Indian provider|  |  File storage |  |   Containers  |
+---------------+  +---------------+  +---------------+  +---------------+

Source control: GitHub   |   Testing: Vitest + Playwright   |   Hosting: AWS
```

### Backend services

The backend is organised into separate services so the communication layer, procurement workflow, queue engine and AI services can scale independently:

- **User Service** – farmers, centre operators, officers and roles
- **Token & Slot Service** – slot booking and digital tokens
- **Queue Service** – live queue state and estimated waiting time
- **Notification Service** – WhatsApp and SMS alerts
- **Prediction Engine** – waiting-time, congestion and arrival forecasts
- **Centre Service** – centre profiles, capacity, staff, storage and transport
- **Report & Analytics Service** – dashboards and reports for centres and government

### WhatsApp + SMS messaging flow

```
Farmer
  |
  v
WhatsApp / SMS gateway
  |
  v
Messaging API
  |
  v
Backend API
  |
  v
Farmer + Centre database
  |
  v
Queue engine + AI model
  |
  v
Response / notification back to the farmer
```

The WhatsApp/SMS sender number is treated as a **replaceable configuration**, not part of the core application logic. During the hackathon a clearly labelled prototype/test account is used; on adoption, the government department can provide and control the production WhatsApp Business and SMS sender configuration.

---

## 🧠 Technology Stack

| Layer               | Technology                                            | Purpose                                                              |
| ------------------- | ----------------------------------------------------- | -------------------------------------------------------------------- |
| **Frontend**        | **Angular + TypeScript**                              | Farmer & Centre web application                                      |
| **UI**              | **Tailwind CSS + Angular Material**                   | Responsive interface                                                 |
| **Forms**           | **Angular Reactive Forms**                            | Registration and booking forms                                       |
| **State**           | **Angular Services + Signals**                        | Application state                                                    |
| **Backend**         | **Node.js + Express.js**                              | REST APIs & business logic                                           |
| **Database**        | **MongoDB + Mongoose**                                | Farmer, crop, centre, booking & procurement data                     |
| **Real-Time**       | **Socket.IO**                                         | Live queue and centre updates                                        |
| **AI**              | **OpenAI API**                                        | AI assistant, natural-language interaction, document/text assistance |
| **Prediction**      | **Node.js-based prediction logic / ML service later** | Queue, waiting-time and overload prediction                          |
| **File Storage**    | **AWS S3**                                            | Documents, receipts and uploaded files                               |
| **Notifications**   | **Firebase Cloud Messaging + SMS Gateway**            | App notifications and SMS                                            |
| **WhatsApp**        | **WhatsApp Business API**                             | Farmer alerts and status updates                                     |
| **Multilingual**    | **Angular i18n / Translation JSON**                   | Marathi, Hindi, English                                              |
| **Voice**           | **Speech-to-Text + Text-to-Speech**                   | Voice-enabled farmer interface                                       |
| **Deployment**      | **AWS**                                               | Hosting and cloud infrastructure                                     |
| **Version Control** | **Git + GitHub**                                      | Team development                                                     |



### Why we chose these technologies

| **Layer**           | **Technology**                             | **Why Chosen / Alternatives Not Preferred**                                                                  |
| ------------------- | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| **Frontend**        | **Angular + TypeScript**                   | Structured, scalable framework; preferred over React/Next.js for an integrated TypeScript-based architecture |
| **UI**              | **Tailwind CSS + Angular Material**        | Fast responsive UI with ready components; avoids building components from scratch                            |
| **Forms**           | **Angular Reactive Forms**                 | Strong validation and structured form handling; preferred over manual form handling                          |
| **State**           | **Angular Services + Signals**             | Built-in Angular approach; avoids adding an extra state-management library                                   |
| **Backend**         | **Node.js + Express.js**                   | Lightweight and fits the TypeScript/JavaScript ecosystem; avoids a separate backend language                 |
| **Database**        | **MongoDB + Mongoose**                     | Flexible document structure; preferred over rigid relational schema during rapid development                 |
| **Real-Time**       | **Socket.IO**                              | Simple real-time communication; preferred over complex custom WebSocket implementation                       |
| **AI**              | **OpenAI API**                             | Strong natural-language capabilities; preferred over maintaining a separate LLM infrastructure               |
| **Prediction**      | **Node.js-based prediction logic**         | Easy integration with backend; avoids unnecessary Python/FastAPI dependency for the prototype                |
| **File Storage**    | **AWS S3**                                 | Scalable and reliable object storage; preferred over storing files directly in the database                  |
| **Notifications**   | **Firebase Cloud Messaging + SMS Gateway** | Supports both app and basic-phone communication; broader reach than app-only notifications                   |
| **WhatsApp**        | **WhatsApp Business API**                  | Familiar communication channel for farmers; reduces dependence on app-only access                            |
| **Multilingual**    | **Angular i18n / Translation JSON**        | Simple and maintainable multilingual implementation; avoids heavy translation frameworks                     |
| **Voice**           | **Speech-to-Text + Text-to-Speech**        | Enables accessible voice interaction; avoids complex custom voice systems                                    |
| **Deployment**      | **AWS**                                    | Scalable cloud infrastructure; suitable for phased deployment and future expansion                           |
| **Version Control** | **Git + GitHub**                           | Standard collaborative development workflow; widely supported and easy to maintain                           |


> The technology stack may be refined as development progresses. Deployment on production would follow the concerned department's approved hosting, data-sharing and retention requirements.

---

## 🤖 AI & Decision Engine

The AI layer has a clearly defined purpose rather than being only a label. The first model predicts **waiting time**; later models add congestion forecasting and centre/slot recommendation.

**What it predicts**
- Expected arrival timing and crop quantity
- Waiting time for every farmer in the queue
- Centre workload distribution and congestion risk
- Capacity and resource requirements

**What it decides (decision engine)**
- Centre recommendation
- Slot allocation and smart slot recommendation
- Resource planning
- Farmer notification, including leave-and-return alerts

**Waiting-time model – input features**
current queue length, arrivals per hour, number of working weighing machines, testing capacity, staff availability, average service time, quantity, historical patterns, storage utilisation and weather indicators.

**Explainable output** – the prediction is broken down into reasons, for example:

```
Predicted extra wait: +28 min
  - Baseline queue ........... +10 min
  - High arrivals ............ +19 min
  - One machine unavailable .. +15 min
```

**Model approach** – start with Python, pandas and scikit-learn on structured data; upgrade to time-series or deep-learning models only if justified. The system begins with verified historical data and rule-based estimates, and improves by comparing forecasts with actual arrivals.

### Bottleneck detection and what-if simulation

The centre is modelled as a pipeline instead of a single queue:

`Arrival → Verification → Quality Testing → Weighing → Procurement → Storage → Transport`

Each stage shows its own queue and capacity, so the system can identify the actual bottleneck. Officials can then simulate:

- Removing one weighing machine and see the change in waiting time
- Increasing arrivals by 50% and see the predicted congestion
- Reducing testing staff and see the new bottleneck
- Adding a truck and see the storage/dispatch improvement
- Redirecting future bookings to another eligible centre and see the effect

### Demo scenario

Start with 3 working weighing machines and a normal queue. Simulate a failure of one machine: the centre view turns from normal to high load, the AI predicts a longer waiting time, the system identifies weighing as the bottleneck and recommends redirecting future bookings to an eligible nearby centre, and the affected farmer receives an SMS/WhatsApp message with the new recommendation.

---

## 🗂️ Data & Data Sources

**Data sources**

- data.gov.in – government open datasets and agriculture statistics
- Agmarknet – mandi/market arrivals, prices and market information
- Maharashtra Food, Civil Supplies and Consumer Protection Department – procurement workflow and state information
- Official/authorised procurement-centre data, where made available by the concerned department

**Prototype data**

Where centre-level historical queue data is unavailable, operational queue variables are **simulated (synthetic)** for the prototype and clearly labelled as such. Public datasets supply market arrivals, prices, and crop and market information. The source and date of every external dataset used is documented.

Synthetic data covers:

- **Farmer level:** farmer_id, centre_id, date, arrival time, appointment time, crop, quantity, service start/end and waiting time
- **Centre / time level:** arrivals, queue at start/end, working scales, testing staff, testing stations, average service time, storage utilisation, trucks and weather
- **Scenarios:** normal day, peak harvest, machine failure, testing-staff shortage, sudden arrival surge, transport shortage and high storage utilisation
- **Target outputs:** waiting time, queue length, congestion level, expected completion time and centre utilisation

**Centre registration data**

Centre ID, name, type, address, district and GPS location · crops handled, operating dates/hours and daily procurement capacity · storage capacity and current utilisation · number of weighing machines (total, operational, capacity, average weighing time) · testing stations, testing staff and average test time · registration, testing, weighing and loading staff availability · transport/truck availability, capacity and pending dispatches · historical throughput and average processing times · centre administrator role and permissions.

---

## 🛠️ Methodology

HexaFarm follows a **farmer-first, agile and data-driven approach**.

**Analyze → Prototype → Develop → Integrate → Pilot Test → Deploy on AWS → Improve**

Development begins with requirement analysis and rapid prototyping, followed by building multilingual registration, AI prediction, centre recommendation, slot booking and payment-tracking modules. WhatsApp, SMS, weather, MSP and maps are then integrated. After pilot testing with farmers and procurement centres, the platform is securely deployed on AWS and continuously improved using operational data and stakeholder feedback.

---

## ✅ Feasibility & Challenges

| Area | Approach |
|---|---|
| **Technical** | Proven, scalable technologies — Node.js, Angular, Express.js, WhatsApp and SMS gateways, secure authentication |
| **Operational** | Phased, centre-wise rollout that fits into existing procurement processes without disrupting operations |
| **Adoption** | WhatsApp for smartphone users and two-way SMS for basic phones, in Marathi, Hindi and English |
| **Scalability** | Modular architecture that can grow from pilot centres to district, state and national networks |
| **Economic** | Cloud-based deployment, reusable modules and digital communication reduce infrastructure cost and manual workload |

### Risks and mitigation

| Risk | Why it matters | Mitigation |
|---|---|---|
| Poor data quality | Bad predictions | Validation, data-quality checks and confidence scores |
| No real queue data | AI cannot be trained directly | Synthetic simulation for the prototype; seek authorised historical data |
| Low smartphone adoption | An app-only solution excludes users | SMS + WhatsApp, with IVR/USSD planned |
| Network outage | Farmer cannot access the online service | SMS where available; kiosk/local sync for centre operations |
| Wrong AI recommendation | Operational harm | Human approval for centre-level actions; show explanations |
| Privacy concerns | Farmer trust and compliance | Data minimisation, access control and encryption |
| Dependency on government systems | Integration delays | Standard APIs and configurable adapters, starting with mock/sandbox environments before authorised live integration |
| Payment complexity | Sensitive financial data | Secure, auditable connections with approved government payment systems, without storing sensitive banking information |

---

## 🔐 Security, Privacy and Governance

- Collect only the information necessary for procurement services
- Separate farmer identity data from analytics wherever possible
- Role-based access for farmers, centre operators, district officers and administrators
- OTP authentication for the prototype; government-approved authentication for production
- Encrypt sensitive data in transit and at rest in production
- Maintain an audit trail for important procurement events
- No real Aadhaar, bank credentials or government credentials are used in the hackathon prototype
- Prototype/synthetic data is clearly labelled
- A government deployment follows the department's approved identity, data-sharing, hosting and retention requirements

---

## 📈 Scalability

The pilot begins with one district and a small number of procurement centres. The architecture then scales to more centres, districts and crops by keeping the communication layer, procurement workflow, queue engine and AI services separate. The production system integrates only with authorised government systems and data sources.

---

## 🧪 Prototype (MVP) Scope

- Farmer registration and centre registration
- Slot booking and token generation
- Shared farmer + centre database
- Live simulated queue
- AI waiting-time prediction
- WhatsApp chatbot
- SMS command and notification system
- Centre dashboard
- One working what-if scenario (weighing-machine failure)
- Marathi / Hindi / English message templates

---

## 🔍 Research

**Primary research – field visit**
District Marketing Office, Shahu Market Yard, Kolhapur. The team interacted with officials and observed the existing procurement workflow — farmer registration, crop arrival, weighing, storage and payment. The visit highlighted gaps in advance demand visibility, farmer communication, queue coordination, capacity planning and procurement tracking, which directly shaped HexaFarm's core features.

**Secondary research**
Existing government platforms and agricultural resources were studied to understand current digital procurement practices, farmer services and market infrastructure:

- e-Kisan Upaj Nidhi (eKUN)
- eSamridhi – Farmer Welfare Portal
- Maharashtra State Agriculture Marketing Board (MSAMB)

---

## 📂 Project Structure


```
KISAN-PRAVAH/
│
├── frontend/          # Angular + TypeScript
├── backend/           # Node.js + Express.js
├── models/            # MongoDB + Mongoose
├── ai/                # OpenAI API
├── prediction/        # Queue / Demand / Capacity Prediction
├── storage/           # AWS S3
├── notifications/     # Firebase / SMS / WhatsApp
├── i18n/              # Multilingual
├── voice/             # Speech-to-Text / Text-to-Speech
├── tests/              # Unit / Integration / E2E
├── docker/             # Docker Configuration
├── .env.example
├── .gitignore
└── README.md
```

---

## 🎯 Expected Impact

| Stakeholder | Impact |
|---|---|
| **Farmers** | Greater control over where and when to sell; less travel, waiting and uncertainty; less dependence on intermediaries; transparent status and payment tracking that improves income stability and confidence |
| **Procurement Centres** | Advance demand visibility for better planning of capacity, manpower, storage and weighing facilities; earlier identification of bottlenecks; better utilisation of weighing and testing capacity; less crowding and congestion |
| **Government** | Real-time, district-level data on demand, procurement gaps, congestion and underused capacity for predictive planning; operational data that supports future planning |

**Overall benefits**

- **Economic** – lower travel and operating costs, better infrastructure utilisation, stable farmer livelihoods
- **Social** – saves time, reduces stress, builds farmer confidence through transparent status information, and gives **equal access to smartphone and basic-phone users**
- **Environmental** – fewer unnecessary journeys, lower fuel consumption, emissions and resource wastage

---

## 🚀 Future Scope

- **More channels** – IVR, USSD and assisted kiosks so smartphone ownership is never a prerequisite
- **Optional farmer app** – a dedicated Flutter / React Native mobile interface for farmers
- **Smarter models** – upgrade to time-series or deep-learning models where justified, plus congestion forecasting and richer centre/slot recommendation
- **Maps and geospatial** – map service and geospatial database for better centre recommendations
- **Government integration** – integration with authorised government agricultural, identity and payment systems
- **Scale-out** – expansion from one district and a few centres to more centres, districts, crops and eventually state and national networks
- **Centre hardware** – configurable device adapters for weighing systems and other centre hardware
- **Analytics** – advanced analytics for procurement authorities

---

## 👥 Team

**Team HexaFarm** — Smart India Hackathon 2026

---

## 📌 Project Status

🚧 Currently under development as part of Smart India Hackathon 2026.
