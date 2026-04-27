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

---

### Preview

🔗 **Live Demo:** [Lupus Together](https://lupustogether.vercel.app/)

> Backend on Render free tier, allow a few seconds on first load.

** ADD THREE MOST PROMINENT SCREENSHOTS **

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

**Front-end testing:**

All core features and UI components have been thoroughly tested for reliability, accessibility, and responsiveness.

**Accessibility Audit:**

- **Purpose:** To enhance inclusivity and usability for all users, ensuring the application is accessible to those using assistive technologies and compliant with **WCAG 2.1 AA** standards.
- **Summary:** Conducted a complete accessibility audit using **Axe DevTools** and **Google Lighthouse**. Key improvements included proper ARIA usage, improved keyboard navigation, better color contrast, and semantic HTML structure across all interactive components.
- **Tools Used:** **Google Lighthouse** (Web Accessibility Audit) and **Axe DevTools** (In-depth Element Level Testing).
- **Results:** The accessibility score improved from **83% to 100%**, ensuring compliance with modern accessibility standards and a more inclusive user experience.

**E2E and QA Testing(Cypress):**

1. **Navbar Scroll functionality:** We implemented an end-to-end test using Cypress to verify the Navbar's scroll behavior:

- Ensures each navigation link scrolls the user to the correct section.
- Handles mobile view by opening the hamburger menu automatically.
- Tested across multiple viewports: _desktop and tablet_.
- Validates smooth scroll and section visibility for a reliable user experience.

2. **Hero CTA Interaction:**

- **TEST:** Hero CTA scroll behavior
- Purpose: Ensure that clicking the Hero "Join Our Community!" CTA scrolls smoothly to the Join section.

3. **Join Form Validation & Submission:**

- Checks inline validation messages for all required fields (first name, last name, email, phone, consent checkbox).
- Validates error handling for invalid inputs.
- Tests successful form submission with valid data and confirms form reset afterward.
- Ensures that duplicate emails trigger the correct error toast and prevent multiple entries.
- Confirms that the _frontend-backend shared secret token handshake_ works as expected during submission.

**Back-end testing (Django + Pytest):**

**Integration tests:**

This section tracks backend tests as they are added. Each test includes a short reason and a status to keep things easy to follow.

| Test Type                         | Description                                                                                                                                                                            | Result |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| Model test                        | Confirms that the CommunityMember model can be created, behaves as expected, and that user details are saved to the database correctly.                                                | PASSED |
| Serializer validation tests       | Ensures that the CommunityMemberSerializer correctly validates input data, enforcing required fields and constraints. Includes checks for missing fields like first_name or last_name. | PASSED |
| Views test                        | Confirms that the `/community/` endpoint correctly handles GET and POST requests with both valid and invalid data.                                                                     | PASSED |
| POST request duplicate email test | Verifies that submitting a POST request with an email that already exists in the database returns a validation error and prevents duplicate entries.                                   | PASSED |

**Security Tests:**

| Test Name                                            | Description                                                                                                                   | Why It’s Useful                                                                                                                                                                                                                | Result |
| ---------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------ |
| **Frontend - Backend Shared Secret Token Handshake** | Verified that requests with the correct shared secret token succeed, and invalid or missing tokens return `401 Unauthorized`. | Protects the backend from unauthorized requests or bots, ensures only your frontend or trusted clients can submit data to sensitive endpoints, and adds a lightweight layer of security even without full user authentication. | PASSED |

---

### Future Plans

- **Scroll-triggered Animations**: for a smoother, more interactive visual experience.
- **Migrate to Astro.js**: for improved app performance and enhanced SEO/GEO capabilities.

---

### Acknowledgment

Inspired by a family member who battles Lupus daily. This project is a tribute to their strength, and to those navigating this journey around the world.

---

### Disclaimer

All names, services, testimonials, locations, and brand references, including _Lupus Together_, are fictional and created for the sole purpose of demonstrating software development, UI/UX design, and implementation best practices. Any resemblance to real individuals or organizations is purely coincidental. _Note: This is project intended to showcase UI/UX thinking, design sensitivity, and modern web development techniques._

Images used are royalty-free and sourced from **[Unsplash](https://unsplash.com/)** and **[Lummi AI](https://www.lummi.ai/)** , optimized for performance (WebP format). **Social links** included are placeholders to demonstrate UI layout and design.

---

### Credits

- **Sole Developer & Designer:** Koveshan Munsami
- **Inspiration:** A family member who lives with Lupus daily. This is for them, and for all who need a gentle place to land.

---

### Contact

- Connect with me on [LinkedIn](https://www.linkedin.com/in/koveshan-munsami/)
