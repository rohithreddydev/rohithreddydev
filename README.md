<img src="app-icon.png" width="72" align="left" />

### Hi, I'm Rohith

Founder-engineer. I design, build, and operate production software solo — most recently
**SmartBiz AI**, a WhatsApp-first AI business manager that's live today with real petrol-station
customers running real money through it.

<br clear="left" />

## What I've built

**SmartBiz AI** is two linked systems, both live in production, both closed-source (real customer
data lives in them, so the code stays private — but here's what's actually running):

- A **React/TypeScript POS and accounting web app**, deployed on Vercel, packaged for Android with
  Capacitor, and published on the Google Play Store — a real double-entry accounting core where
  every rupee is stored as integer paise, never a float.
- A companion **WhatsApp bot** (Node.js/Express) that lets a shop owner run their business by
  texting it naturally — "add 500 fuel expense," "who owes me money" — powered by a Groq-hosted
  LLM for intent parsing and Google Gemini's vision model for reading photographed bills and
  receipts. The bot sanitizes inputs and checks model-generated intent names against an
  allowlist before routing them to business-specific handlers. The public ledger demo below
  separately demonstrates explicit action, account, and amount validation with synthetic data.

<p float="left">
  <img src="dashboard.png" width="260" />
  <img src="inventory.png" width="260" />
</p>

🌐 **[smartbizai.in](https://smartbizai.in)** &nbsp;·&nbsp; 📱 **[Google Play](https://play.google.com/store/apps/details?id=in.smartbizai.app)**

**Also currently building: petrol-station CCTV analytics** — a
YOLOv8-based edge computer-vision system for petrol-station CCTV. An iterative fine-tuning loop
(each model version auto-labels the next batch of frames, retrains, gets visually compared
before/after) feeds a live deployment that pulls RTSP from the station's existing 5-channel DVR,
logs person/car/motorcycle/truck counts to SQLite, and produces weekly traffic reports. The source repository stays private. Operational footage and datasets are kept outside
Git history.

## Public code you can actually read

Since the production systems above are closed-source, here's where the same patterns show up in
the open, built from scratch with synthetic data:

- **[agentic-ledger-demo](https://github.com/rohithreddydev/agentic-ledger-demo)** — the
  prompt-injection guard architecture from the WhatsApp bot, extracted and rebuilt: LLM intent
  parsing, a strict allowlist validator, and a double-entry ledger that never trusts the model's
  raw output. MIT-licensed, 17 passing tests.
- **[doctoolkit](https://github.com/rohithreddydev/doctoolkit)** — an offline-first Android
  document toolkit (PDF/Word conversion, image tools, QR/barcode scanner). Core document processing runs on-device, including a bundled OCR engine.
  📱 [Get it on Google Play](https://play.google.com/store/apps/details?id=com.smartbizai.doctoolkit)

## What I work with

React, TypeScript, Node.js, Postgres/Supabase, LLM-based agents (intent parsing, guardrails, tool
use), Android/Capacitor, computer vision fundamentals (YOLOv8).

🔍 Currently looking for my next role in **AI / agentic engineering**.

🔗 [LinkedIn](https://www.linkedin.com/in/rohithreddydev/) &nbsp;·&nbsp; [smartbizai.in](https://smartbizai.in)
