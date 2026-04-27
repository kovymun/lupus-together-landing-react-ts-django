## Lupus Together

> A full-stack awareness platform for the Lupus community, built in honour of a family member living with the condition, powered by React + TypeScript, Django REST API, and deployed on Vercel + Render.

---

### Table of Contents

- [Preview](#preview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Performance](#performance)
- [Security](#security)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
- [Testing](#testing)
- [Future Plans](#future-plans)
- [Credits & Contact](#credits--contact)

---

### Preview

🔗 **Live Demo:** [Lupus Together](https://lupustogether.vercel.app/)

> Backend on Render free tier, allow a few seconds on first load.

<p align="center">
  <img width="250" alt="lt-hero" src="https://github.com/user-attachments/assets/c503a1f7-f6dc-4cf4-9e4a-e289fd04de59" />
  <img width="250" alt="lt-social-proof" src="https://github.com/user-attachments/assets/a68d81e9-1b84-48a4-93f2-ebaba5200edc" />
  <img width="250" alt="lt-form" src="https://github.com/user-attachments/assets/bff2507e-29b3-4e39-a0f0-ad2dbc8b96ed" />
</p>

---

### Tech Stack

**Frontend:**
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white) ![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat&logo=css3&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)

**Backend:**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![Django](https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

**Testing & QA:**
![Cypress](https://img.shields.io/badge/Cypress-17202C?style=flat&logo=cypress&logoColor=white) ![Axe DevTools](https://img.shields.io/badge/Axe%20DevTools-663399?style=flat&logo=axe&logoColor=white) ![Google Lighthouse](https://img.shields.io/badge/Google%20Lighthouse-F44B21?style=flat&logo=lighthouse&logoColor=white)

---

### Features

- **Accessibility:** WCAG 2.1 AA, audited from 83% to 100% using Axe DevTools and Lighthouse.
- **Typography:** Fluid layout with CSS `clamp()` across mobile, tablet, and desktop.
- **Theming:** Automatic light/dark theme detection.
- **Validation:** Full-stack form validation with duplicate entry protection.
- **Security:** Secure POST submissions via a shared-secret token handshake.
- **Testing:** E2E tested with Cypress across desktop and tablet viewports.

---

### Performance

Audited with Google Lighthouse:

| Metric             | Score |
| ------------------ | ----- |
| **Performance**    | 95+   |
| **Accessibility**  | 100   |
| **Best Practices** | 100   |
| **SEO**            | 100   |

---

### Security

| Feature                   | Description                                                                                                      |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Shared Secret Token**   | Frontend includes a secret key in `.env`. Verified by the backend on every request to block unauthorized access. |
| **Serializer Validation** | All incoming data passes through DRF serializers before saving, preventing malformed or malicious input.         |
| **CORS Policy**           | Restricted to trusted origins only, not Django's default open configuration.                                     |

---

### Getting Started

#### Prerequisites

- [Node.js](https://nodejs.org/en) v18+
- [Docker Desktop](https://www.docker.com/products/docker-desktop) installed and running
- `.env` file required in both `frontend/` and `backend/` — see `.env.example` for reference

#### Quick Start (Full Stack)

```bash
git clone https://github.com/kovymun/lupus-together-landing-react-ts-django.git
cd lupus-together-landing-react-ts-django-main
npm install
npm start
```

Frontend runs on `http://localhost:5173` · Backend runs on `http://localhost:8000`

#### Run Individually

**Frontend only:**

```bash
npm run dev
```

**Backend only:**

```bash
cd backend
docker-compose up
```

> If you modify backend dependencies or the Dockerfile, rebuild first:

```bash
docker-compose build && docker-compose up
```

---

### Testing

**E2E Testing (Cypress):**

| Test            | Coverage                                                                             |
| --------------- | ------------------------------------------------------------------------------------ |
| Navbar scroll   | All nav links, hamburger menu, desktop and tablet viewports                          |
| Hero CTA        | Scrolls correctly to Join section                                                    |
| Join form       | Field validation, error handling, submission, form reset, duplicate email protection |
| Token handshake | Valid token succeeds · invalid or missing token returns `401 Unauthorized`           |

**Backend Integration Tests (pytest):**

| Test                      | Result    |
| ------------------------- | --------- |
| Model                     | ✅ PASSED |
| Serializer validation     | ✅ PASSED |
| Views · GET & POST        | ✅ PASSED |
| Duplicate email rejection | ✅ PASSED |

---

### Future Plans

- **Scroll-triggered Animations:** smoother, more interactive visual experience.
- **Migrate to Astro.js:** improved performance and enhanced SEO/GEO capabilities.

---

### Credits & Contact

**Developer & Designer:** [Koveshan Munsami](https://www.linkedin.com/in/koveshan-munsami/)

Built in honour of a family member living with Lupus daily.

**Disclaimer:** All names, testimonials, and brand references are fictional, created solely to demonstrate software development and UI/UX best practices. Images sourced from [Unsplash](https://unsplash.com/) and [Lummi AI](https://www.lummi.ai/), optimized for performance in WebP format.

---
