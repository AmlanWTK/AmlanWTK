<div align="center">

<img src="assets/hero.svg" width="100%" alt="Amlan Sarkar — Full-stack × AI systems engineer. Products shipped end to end. AI that is grounded, guarded and measured.">

<a href="mailto:amlansarkar738@gmail.com"><img src="assets/btn-email.svg" height="34" alt="Email"></a>&nbsp;
<a href="https://www.linkedin.com/in/amlansarkar-dev/"><img src="assets/btn-linkedin.svg" height="34" alt="LinkedIn"></a>&nbsp;
<a href="https://amlanwtk.github.io/Portfolio/"><img src="assets/btn-portfolio.svg" height="34" alt="Portfolio"></a>

<br>

<img src="assets/terminal.svg" width="100%" alt="Terminal — whoami: Full-stack engineer, AI systems builder. Focus: AI products with a deterministic layer around the model. Domains: clinical, legal, commerce, medical imaging.">

</div>

<br>

<img src="assets/divider.svg" width="100%" alt="">

### Featured work

Six repositories, chosen the way an engineering lead would pick them: what it does, why it's hard, how it's built, and what you can go and inspect.

<table>
<tr><td>
<a href="https://github.com/AmlanWTK/Dataloom"><img align="left" src="assets/tile-dataloom.svg" width="166" alt="Dataloom"></a>
<b><a href="https://github.com/AmlanWTK/Dataloom">Dataloom</a></b> — ask your data questions in plain English<br>
<b>Problem</b> &nbsp;Analysts want to query in English. Handing an LLM a database connection is a security hole.<br>
<b>How</b> &nbsp;Gemini drafts the SQL; a deterministic <code>sqlglot</code> AST validator rejects mutations, injections and forbidden statements before Postgres ever sees it, and external connections are forced read-only at the transport layer. Results stream over SSE into ECharts; a pandas profiler grounds the AI's explanations so it cites only computed numbers.<br>
<b>Proof</b> &nbsp;60 tests across 11 suites, 16 on the validator alone · <a href="https://dataloom-psi.vercel.app">Live demo</a> · <a href="https://github.com/AmlanWTK/Dataloom">Source</a><br>
<code>Next.js 15</code> <code>FastAPI</code> <code>sqlglot</code> <code>PostgreSQL</code> <code>Gemini</code>
</td></tr>
<tr><td>
<a href="https://github.com/AmlanWTK/clausewise"><img align="left" src="assets/tile-clausewise.svg" width="166" alt="ClauseWise"></a>
<b><a href="https://github.com/AmlanWTK/clausewise">ClauseWise</a></b> — observability and evaluation for RAG<br>
<b>Problem</b> &nbsp;Retrieval systems fail silently. You can't fix what you can't trace.<br>
<b>How</b> &nbsp;Per-query traces with retrieval and rerank scores, per-stage latency and cost, over 510 CUAD contracts in pgvector (HNSW) with local <code>bge-small</code> embeddings. A 117-question eval split, frozen before tuning, runs across all 8 chunking × retrieval × reranking configurations; the cross-encoder reranker measurably hurt, so it's off by default. Refuses to answer below a confidence threshold.<br>
<b>Proof</b> &nbsp;Eval results committed to the repo, CI on every push · <a href="https://github.com/AmlanWTK/clausewise">Source</a><br>
<code>FastAPI</code> <code>React</code> <code>pgvector</code> <code>sentence-transformers</code> <code>PostgreSQL</code>
</td></tr>
<tr><td>
<a href="https://github.com/AmlanWTK/ChartWright"><img align="left" src="assets/tile-chartwright.svg" width="166" alt="ChartWright"></a>
<b><a href="https://github.com/AmlanWTK/ChartWright">ChartWright</a></b> — clinical document intelligence &nbsp;<code>checkpoint 14 / 34</code><br>
<b>Problem</b> &nbsp;Prior-auth packets, referrals and lab reports arrive as scans and faxes. Extracting them by hand is slow; extracting them by LLM is unverifiable.<br>
<b>How</b> &nbsp;A cost-aware VLM cascade routes each document to the cheapest capable model. A grounding contract makes every extracted field carry a bounding box, source span and confidence; low-confidence fields go to human review; policy reasoning is retrieval-only. Temporal workflows, Kafka, MinIO, DB-enforced tenant isolation, append-only audit log, <code>mypy --strict</code>, 80% coverage gate in CI.<br>
<b>Proof</b> &nbsp;Walking skeleton complete, classification module live · <a href="https://github.com/AmlanWTK/ChartWright">Source</a><br>
<code>Python 3.12</code> <code>Temporal</code> <code>Kafka</code> <code>PostgreSQL</code> <code>VLMs</code>
</td></tr>
<tr><td>
<a href="https://github.com/AmlanWTK/lume-commerce"><img align="left" src="assets/tile-lume.svg" width="166" alt="Lumè"></a>
<b><a href="https://github.com/AmlanWTK/lume-commerce">Lumè</a></b> — multi-vendor commerce, all four roles<br>
<b>Problem</b> &nbsp;Most "e-commerce" portfolio projects stop at a cart. Real platforms have sellers, admins, refunds and webhooks that fire twice.<br>
<b>How</b> &nbsp;Guest → customer → seller → admin. Typo-tolerant search, faceted filters, inventory reservations, four payment providers (Stripe, PayPal, SSLCommerz, COD) behind idempotent webhooks, Upstash rate limiting, verified-purchase reviews, seller analytics, admin controls. Vitest and Playwright in GitHub Actions.<br>
<b>Proof</b> &nbsp;20 of 20 planned checkpoints shipped · <a href="https://lume-commerce-zeta.vercel.app">Live demo</a> · <a href="https://github.com/AmlanWTK/lume-commerce">Source</a><br>
<code>Next.js 15</code> <code>Drizzle</code> <code>Clerk</code> <code>Stripe</code> <code>PostgreSQL</code>
</td></tr>
<tr><td>
<a href="https://github.com/AmlanWTK/ArchLens"><img align="left" src="assets/tile-archlens.svg" width="166" alt="ArchLens"></a>
<b><a href="https://github.com/AmlanWTK/ArchLens">ArchLens</a></b> — AI system-design reviewer<br>
<b>Problem</b> &nbsp;Architecture reviews need a principal engineer. Most teams don't have one on call.<br>
<b>How</b> &nbsp;Upload a PNG, PDF or Mermaid diagram. Gemini's vision model returns structured JSON scored across eight dimensions with ranked issues and effort-estimated fixes; the app rebuilds the diagram in Mermaid, renders a redesign and exports the review to PDF. Clerk auth, Prisma on Neon, UploadThing storage, explicit job lifecycle management.<br>
<b>Proof</b> &nbsp;<a href="https://arch-lens-vert.vercel.app">Live demo</a> · <a href="https://github.com/AmlanWTK/ArchLens">Source</a><br>
<code>Next.js 15</code> <code>React 19</code> <code>Gemini Vision</code> <code>Prisma</code> <code>Mermaid</code>
</td></tr>
<tr><td>
<a href="https://github.com/AmlanWTK/Beacon"><img align="left" src="assets/tile-beacon.svg" width="166" alt="Beacon"></a>
<b><a href="https://github.com/AmlanWTK/Beacon">Beacon</a></b> — a distributed URL shortener, written from scratch in Go<br>
<b>Problem</b> &nbsp;A deliberate forcing function: build the whole service, not just the handler.<br>
<b>How</b> &nbsp;Standard-library <code>net/http</code> routing, Redis cache-aside with Postgres failover, sliding-window rate limiting, JWT + bcrypt auth with roles, click analytics with referrer tracking, DNS-verified custom domains, on-demand QR codes, Swagger docs, rotating logs.<br>
<b>Proof</b> &nbsp;Phase 8 of 9 complete, deployment next · <a href="https://github.com/AmlanWTK/Beacon">Source</a><br>
<code>Go 1.26</code> <code>PostgreSQL</code> <code>Redis</code> <code>JWT</code> <code>OpenAPI</code>
</td></tr>
</table>

<sub><b>Also:</b> <a href="https://github.com/AmlanWTK/apexledger">ApexLedger</a> — real-time crypto dashboard in Flutter, Binance WebSockets parsed in Dart isolates (<a href="https://vimeo.com/1200402641">video</a>) · <a href="https://github.com/AmlanWTK/flutter_offline_doc">Offline Doc Chat</a> — on-device OCR and Q&amp;A, English and Bangla, nothing leaves the phone · <a href="https://github.com/AmlanWTK/grounded-legal-drafting-assistant">Grounded Legal Drafting</a> — sourced case-fact summaries with Gemini and ChromaDB</sub>

<br><br>

<img src="assets/divider.svg" width="100%" alt="">

### AI engineering

The difference between calling a model and building a system is what sits around the model. Every claim below points at a repository.

| Capability | Where | What's actually there |
|---|---|---|
| **Guarded generation** | Dataloom | Model output parsed into an AST and checked against a deterministic allowlist; read-only DB role as a second wall; 16 dedicated injection and mutation tests |
| **Retrieval & vector search** | ClauseWise | pgvector with HNSW, local `bge-small` embeddings on CPU, hybrid dense + full-text mode, cross-encoder reranking — measured, and switched off when it hurt |
| **Evaluation** | ClauseWise · ChartWright · MRI-RobustSeg | Frozen 117-question split across 8 configs · evaluation-as-infrastructure gating model changes in CI · 10-pair controlled protocol with per-subject scores |
| **Multimodal / VLM pipelines** | ChartWright · ArchLens | Cost-aware model cascade with bounding-box grounding on every field · vision-to-structured-JSON review of architecture diagrams |
| **Grounded answers** | Dataloom · Grounded Legal Drafting | Explanations cite only profiler-computed numbers · summaries carry source evidence from ChromaDB retrieval |
| **Production integration** | Dataloom · ClauseWise · ChartWright | SSE streaming, per-stage latency and cost tracking, rate limits, Temporal workflows, Kafka, append-only audit logs |

<br>

<img src="assets/divider.svg" width="100%" alt="">

### Architecture

One diagram, chosen because it's the pattern that repeats across the AI work: the model proposes, a deterministic layer decides.

<img src="assets/architecture.svg" width="100%" alt="Dataloom architecture: Browser → FastAPI → Gemini drafts SQL → sqlglot AST validator → PostgreSQL (read-only role); results stream back over SSE; mutations and injections are refused at the validator.">

<br>

<img src="assets/divider.svg" width="100%" alt="">

### Building now

<img src="assets/status.svg" width="100%" alt="Build status: ChartWright at checkpoint 14 of 34 (41%); DTHCMS at checkpoint 11 of 160 (7%).">

**[ChartWright](https://github.com/AmlanWTK/ChartWright)** is detailed under Featured work. **[DTHCMS](https://github.com/AmlanWTK/DTHCMS)** is a bilingual (বাংলা / English) clinical operating system for a diabetes, thyroid and hormone practice — Go modular monolith, Next.js web, Expo stations, append-only event ledger, PHI redaction at build time and at runtime. The checkpoint numbers are real and they update when the work does.

<br>

<img src="assets/divider.svg" width="100%" alt="">

### Research

**[MRI-RobustSeg](https://github.com/AmlanWTK/MRI-RobustSeg)** — I took a reported +0.047 Dice improvement from physics-based MRI augmentation and pulled it apart. Roughly +0.032 of it was training budget. Under a controlled protocol across 10 model pairs, the augmentation *costs* 0.006 whole-tumour Dice — 95% CI [−0.008, −0.004], p = 1.2e-4, 0 of 10 pairs positive — and the deficit holds on 895 out-of-distribution subjects. Under review at IEEE JBHI.

**[neuro-or-noise](https://github.com/AmlanWTK/neuro-or-noise)** — Is gamma-band EEG measuring depression, or measuring muscle? A reproduction and artifact audit of a published 99.6%-accuracy MDD-from-EEG claim, built to separate neural signal from EMG and impedance artifacts using subject-wise validation. Companion code for an ICASSP 2027 submission.

<br>

<img src="assets/divider.svg" width="100%" alt="">

### Stack

Only what's in the repositories above.

<table>
<tr><td align="right"><sub><b>LANGUAGES</b></sub></td><td><img src="https://skillicons.dev/icons?i=ts,py,go,dart,cpp&theme=dark" height="40" alt="TypeScript, Python, Go, Dart, C++"></td></tr>
<tr><td align="right"><sub><b>WEB &amp; MOBILE</b></sub></td><td><img src="https://skillicons.dev/icons?i=nextjs,react,tailwind,flutter&theme=dark" height="40" alt="Next.js, React, Tailwind, Flutter"></td></tr>
<tr><td align="right"><sub><b>BACKEND</b></sub></td><td><img src="https://skillicons.dev/icons?i=fastapi,prisma,nodejs&theme=dark" height="40" alt="FastAPI, Prisma, Node.js"></td></tr>
<tr><td align="right"><sub><b>AI / ML</b></sub></td><td><img src="https://skillicons.dev/icons?i=pytorch,sklearn&theme=dark" height="40" alt="PyTorch, scikit-learn"></td></tr>
<tr><td align="right"><sub><b>DATA</b></sub></td><td><img src="https://skillicons.dev/icons?i=postgres,redis,kafka,supabase&theme=dark" height="40" alt="PostgreSQL, Redis, Kafka, Supabase"></td></tr>
<tr><td align="right"><sub><b>INFRA</b></sub></td><td><img src="https://skillicons.dev/icons?i=docker,githubactions,vercel,git&theme=dark" height="40" alt="Docker, GitHub Actions, Vercel, Git"></td></tr>
</table>

<sub>Also in daily use, no icon available: Drizzle · SQLAlchemy · pgvector · sqlglot · Temporal · sentence-transformers · MNE · Neon · Render</sub>

<br><br>

<img src="assets/divider.svg" width="100%" alt="">

### Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/AmlanWTK/AmlanWTK/output/github-snake-dark.svg">
  <img src="https://raw.githubusercontent.com/AmlanWTK/AmlanWTK/output/github-snake.svg" width="100%" alt="Contribution graph">
</picture>

<br>

<img src="assets/divider.svg" width="100%" alt="">

<div align="center">

<br>

**Building intelligent software at the intersection of full-stack and AI engineering — in domains where it has to be right.**

<br>

<a href="mailto:amlansarkar738@gmail.com"><img src="assets/btn-email.svg" height="34" alt="Email"></a>&nbsp;
<a href="https://www.linkedin.com/in/amlansarkar-dev/"><img src="assets/btn-linkedin.svg" height="34" alt="LinkedIn"></a>&nbsp;
<a href="https://amlanwtk.github.io/Portfolio/"><img src="assets/btn-portfolio.svg" height="34" alt="Portfolio"></a>

<br>

<sub>amlansarkar738@gmail.com · <a href="https://github.com/AmlanWTK">github.com/AmlanWTK</a></sub>

</div>
