# 🛫 Hermes – The Elite AI Travel Assistant for SkyLink Airways

## 🌐 Inya.ai Buildathon – Phase 2 Submission

**Hermes** is an advanced **AI-powered travel assistant** designed for **SkyLink Airways** as part of Phase 2 of the *Automation Using Agentic AI – Let Intelligence Take the Lead* Buildathon.

Built on **agentic AI principles**, Hermes delivers a **frictionless, proactive, and hyper-precise** customer experience across multiple channels, showcasing how AI can automate complex, transactional workflows in the aviation industry.

---

## 🚀 What is Hermes?

Hermes is **not just a chatbot**—it is a **proactive, multi-channel AI agent** that acts as a trusted travel advisor.

Inspired by the **Greek god of travel and communication**, Hermes manages the **entire spectrum of pre-flight customer interactions** with unmatched precision and efficiency.

---

## ✨ Core Capabilities

Hermes specializes in three high-impact airline functions:

### 1️⃣ Flight Booking

* Collects all key details (origin, destination, dates, passengers, trip type, cabin class).
* Presents **at least 3 enriched flight options** with stops, fare families, baggage, and fares.
* Supports refinements: non-stop only, cheapest, earliest/latest.
* Simulates booking with **mock PNR generation** and itinerary confirmation.

### 2️⃣ Flight Status Check

* Verifies with **PNR + Last Name**.
* Provides schedule, gate, delay info, and proactive **rebooking options**.
* Offers **real-time SMS alert subscriptions** for updates.

### 3️⃣ Booking Cancellation

* Secure **identity verification**.
* Applies **fare rules & cancellation policies** transparently.
* Breaks down **fees and refund amounts** itemized.
* Requires **explicit confirmation** for irreversible steps.
* Suggests rebooking assistance post-cancellation.

---

## 💡 Why Hermes is Elite

* 🔮 **Proactive & Anticipatory** → Suggests next best actions before asked.
* 🎯 **Hyper-Precision** → 100% accuracy in fares, rules, and financials.
* 📡 **Multi-Channel Presence** → Seamless across:

  * **Voice** (real-time calls)
  * **SMS** (quick alerts & queries)
  * **WhatsApp** (full two-way conversations)
* 🙋 **Personalization** → Uses pre-call variables (`user_name`, `customer_tier`) for tailored greetings.
* 🛡️ **Robust Error Handling** → Recovers gracefully, with **smooth human handoff** including context transfer.
* 🔗 **Automated Post-Call Workflows** → Triggers backend processes like **confirmation emails** via API calls.

---

## ⚙️ Technical Stack

Hermes was built by integrating **Inya.ai Agentic AI** with best-in-class services:

* **Agent Platform:** Inya.ai
* **Foundation LLM:** Google **Gemma-3-27B**

  * *Temperature:* `0.2` (precision-first)
  * *Max Tokens:* `250`
* **Speech-to-Text:** Gnani Transcriber

  * Optimized for Indian accents
  * Interruptions enabled for natural flow
* **Text-to-Speech:** GnaniPro (formal Indian English)
* **Knowledge Base:** Beeceptor-hosted mock APIs

  * `airports.json` (airport codes & cities)
  * `fare_rules.json` (cancellation/change policies)
  * `flights.json` (detailed schedules & fares)
* **Communication (via Twilio):**

  * Voice calls
  * SMS alerts
  * WhatsApp Sandbox messaging
* **Automation:** Post-call trigger to Beeceptor endpoint (e.g., mock confirmations)
* **Analytics:** Call dispositions track intent, PNRs, handoffs, and monetary values

---

## 🛠️ Setup & Deployment

1. **Clone the Repo**

   ```bash
   git clone [Your_GitHub_Repo_URL]
   cd [Your_Repo_Name]
   ```

2. **Configure Mock Data**

   * `knowledge_base` contains sample JSON (`airports.json`, `fare_rules.json`, `flights.json`).
   * Serve via Beeceptor and connect endpoints in Inya.ai.

3. **Inya.ai Agent Setup**

   * Use the detailed `System Prompt` (see `docs/system_prompt.md`).
   * Add Twilio **SID** and **Auth Token**.
   * Point WhatsApp Sandbox webhook → Inya.ai endpoint.

4. **Test Hermes**

   * Place a **call** to your Twilio number.
   * Send an **SMS** query.
   * Join Twilio WhatsApp Sandbox → test via **WhatsApp messaging**.

---

## 🎥 Demo

📽️ [Demo Video Link](#) *(Replace with your actual demo URL)*

Experience Hermes handling **bookings, cancellations, and real-time status checks** across multiple channels.

---

## 🏆 Conclusion

Hermes embodies the Buildathon principles:

**Build Bold. Ship on Time. Surprise Us.**

By transforming **complex airline customer service workflows** into a **seamless, AI-driven experience**, Hermes sets a new standard for intelligent travel assistance.

---
