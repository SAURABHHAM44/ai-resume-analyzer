# AI Resume Analyzer

AI Resume Analyzer is a modern, full‑stack web app that analyzes resumes against job descriptions to generate actionable, AI‑powered feedback. It scores ATS match, highlights missing keywords, extracts skills/experience, and suggests tailored improvements to boost shortlisting chances. Built with React Router, TypeScript, TailwindCSS, and a production-ready server, it supports server-side rendering, fast HMR, and clean deployment workflows.

## Features
- AI Feedback: Instant, role‑aware suggestions to improve resume alignment.
- ATS Match Scoring: Quantified compatibility with job descriptions and required keywords.
- Keyword Insights: Missing and weak keywords highlighted for quick fixes.
- Section Analysis: Experience, skills, projects, and education coverage checks.
- PDF Handling: Upload PDF resumes; conversion and preprocessing supported.
- Cloud Storage: Persist resume files and analysis results securely.
- Key-Value Storage: Cache and reuse analysis for quick iterations.
- Responsive UI: Clean, fast interface styled with TailwindCSS.
- Server-Side Rendering: Fast initial loads and SEO-friendly pages.
- Hot Module Replacement: Developer-efficient iteration with Vite + HMR.

## Tech Stack
- Frontend: React Router, TypeScript, TailwindCSS
- Build: Vite with asset bundling and optimization
- Server: Production-ready app server (SSR enabled)
- Storage: Cloud object storage + key-value store
- Containerization: Docker for reproducible builds and deploys

## Getting Started

### Prerequisites
- Node.js and npm installed
- Optional: Docker for containerized runs

### Installation
Install dependencies:
```bash
npm install
```

### Development
Start the development server with HMR:
```bash
npm run dev
```
Your application will be available at
```
http://localhost:5174/
```

### Building for Production
Create a production build:
```bash
npm run build
```

### Deployment

#### Docker Deployment
Build and run using Docker:
```bash
docker build -t ai-resume-analyzer .
# Run the container
docker run -p 3000:3000 ai-resume-analyzer
```
Deployable to AWS ECS, Google Cloud Run, Azure Container Apps, DigitalOcean App Platform, Fly.io, Railway.

#### DIY Deployment
The built-in app server is production-ready. Deploy the output of `npm run build`:
```
├── package.json
├── package-lock.json (or pnpm-lock.yaml, or bun.lockb)
├── build/
│   ├── client/  # Static assets
│   └── server/  # Server-side code
```

## Usage Flow
1. Upload Resume (PDF)
2. Paste Job Description
3. Run Analysis
4. Review: ATS score, missing keywords, strengths/weaknesses per section, actionable suggestions
5. Iterate and re-run to improve match

## Roadmap
- Multi‑resume comparisons for a single role
- Export annotated feedback PDF
- JD parsing from URLs
- Profile history and versioning
- Fine‑tuned models for domain‑specific roles

## About
- Live: ai-resume-analyzer-omega-eight.vercel.app
- Built with ❤️ using React Router
