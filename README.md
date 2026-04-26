## Lupus Together Community Website: React + TypeScript Frontend | Python Django Backend | Neon Serverless PostgreSQL

> A full-stack awareness platform for the Lupus community, built in honour of a family member living with the condition, powered by React + TypeScript, Django REST API, and deployed on Vercel + Render.

---

### Table of Contents

- [Preview](#preview)
- [Tech Stack](tech-stack)

---

### Preview

🔗 **Live Demo:** [Lupus Together](https://lupustogether.vercel.app/)

> Backend on Render free tier, allow a few seconds on first load.

** ADD THREE MOST PROMINENT SCREENSHOTS **

---

### Highlights

- Thoughtful UI/UX, SEO optimization, and accessibility-first design (WCAG 2.1 AA)
- Fully responsive design with intuitive navigation (React Scroll)
- Modern frontend engineering (React, TypeScript, Vite)
- Secure backend API architecture (Django + DRF, serializer validation)
- Real-world deployment pipeline (Vercel, Render, Neon Serverless PostgreSQL)
- Integration, E2E, and quality testing (Cypress, pytest, Axe, Lighthouse)

---

### Features

1. Smooth section navigation using **React Scroll**.
2. Fully responsive layout across mobile, tablet, and desktop.
3. Content-first, SEO-optimized, accessibility-focused UI/UX.
4. Modern CSS architecture: Grid, Flexbox, and fluid typography (`clamp()`).
5. Automatic light/dark theme detection.
6. WCAG 2.1 AA aligned accessibility implementation.
7. Full-stack form validation (frontend + backend).
8. Secure POST submissions via a **shared-secret token handshake**.

---

### Tech Stack

**Frontend:**
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white) ![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat&logo=css3&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)

**Backend:**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![Django](https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

**Testing & QA:**
![Cypress](https://img.shields.io/badge/Cypress-17202C?style=flat&logo=cypress&logoColor=white) ![Axe DevTools](https://img.shields.io/badge/Axe%20DevTools-663399?style=flat&logo=axe&logoColor=white) ![Google Lighthouse](https://img.shields.io/badge/Google%20Lighthouse-F44B21?style=flat&logo=lighthouse&logoColor=white)

---

### Installation Guide

Follow these steps to set up the project on your local machine, and run both the frontend and backend locally.

#### Pre-requisites:

- **Node.js** (v18 or later), which includes npm by default. [Node.js](https://nodejs.org/en)
- **Docker Desktop** installed and running on your machine. [Docker Desktop](https://www.docker.com/products/docker-desktop).
- **Concurrently** is included as a dependency in this project, so no global installation is required.
- Ensure you create your own `.env` file in the `frontend` and `backend` folders to store secrets and sensitive credentials.

#### Steps:

1. **Create a directory for the project:** Open your terminal and run mkdir `<your-directory-name>` | cd `<your-directory-name>`.
2. **Open the folder in VS Code:** run `code .`
3. **Clone the repository:** git clone https://github.com/kovymun/lupus-together-landing-react-ts-django.git
4. **Navigate into the project folder:** cd lupus-together-landing-react-ts-django-main
5. **Install frontend dependencies:** npm install or npm i
6. **Start the development server:** Navigate to the root folder, and run `npm start`. The app should now be running locally on localhost in the browser of your choice.

**Optional Frontend only:**
`npm run dev`

**Optional Backend only:**

```
cd backend
docker-compose up
```

**Backend setup notes:** If you make changes to backend dependencies or the Dockerfile, rebuild the container. Your backend will run on http://localhost:8000. Ensure Docker Desktop is running before starting the project, otherwise the backend container will fail to start.

```
cd backend
docker-compose build
docker-compose up
```

---

### Usage Guide

This website/landing page is structured into several key sections designed to guide visitors and create a meaningful experience:

- Hero Section
- About Lupus Together
- Understanding Lupus
- Testimonial Section
- Meet the Team
- Join the Community Form
- Footer with contact and legal info

#### How to Use:

1. **Start the Application:** Set up and run the project locally using the steps in the [Installation Guide](#installation-guide), or explore the live site here: [Lupus Together](https://lupustogether.vercel.app/).
2. **Explore the Hero Section:** Once the app loads, you’ll be welcomed with a hero banner representing Lupus Together.
3. **Navigate Smoothly:** Scroll or click through the navigation bar to explore each section. Smooth scrolling is enabled for a seamless experience.
4. **Learn About Lupus Together:** Get to know the purpose behind the platform, what it offers, how it started, and how it supports individuals and families.
5. **Understand Lupus:** The _Understanding Lupus_ section presents facts in a warm, accessible tone, empowering users with knowledge.
6. **Feel the Human Stories:** The testimonial section features powerful community voices to help users feel seen and connected.
7. **Meet the Team:** Discover the faces behind the platform, the people dedicated to fostering support.
8. **Join the Community:** Fill out the form to express interest in becoming part of the Lupus Together support circle.

---

### Production Deployment

This project is deployed using modern, production capable platforms using free tier plans, and configured for real world demonstration. You can access the live application here: [Lupus Together](https://lupustogether.vercel.app/)

1. **Frontend (React + TypeScript):** Deployed on **Vercel** using its free tier, providing fast static delivery and global CDN caching.
2. **Backend (Django REST API):** Hosted on **Render** (free tier) with automatic builds and zero downtime deploys during updates.
3. **Database:** Backed by **Neon Serverless PostgreSQL** (free tier): a cloud native, scalable database service. [Neon](https://neon.com/)

**Note:** This deployment uses free tier plans suitable for demonstration. While the stack is production capable, free tiers may introduce limits such as sleeping or reduced performance under heavy load, but the deployment architecture follows industry standard practices.

---

### Screenshots

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 16px;">

  <img src="https://github.com/user-attachments/assets/05e3200e-2292-46a8-8406-d82d31184281" alt="Lupus Together Hero section" />

  <img src="https://github.com/user-attachments/assets/cb6f361f-b895-4383-81bd-814cad9ff855" alt="Lupus Together About section" />

  <img src="https://github.com/user-attachments/assets/896c5ea3-a8c7-40a5-adc6-e4ef93a12e13" alt="Lupus Together Understanding Lupus section" />

  <img src="https://github.com/user-attachments/assets/ea950122-8ca7-4bf0-87d1-8dfac3efcfae" alt="Lupus Together Testimonial section" />

  <img src="https://github.com/user-attachments/assets/49389ba8-c0b6-4ba0-8063-888f8387f89b" alt="Additional screenshot" />

  <img src="https://github.com/user-attachments/assets/8c1d78f0-b7eb-4508-b6e3-cb1b2a102cc2" alt="Additional screenshot" />

</div>

---

### Security

**Backend Security Measures**

| Security Feature                           | Description                                                                                   | Why                                                       |
| ------------------------------------------ | --------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| **Frontend - Backend Shared Secret Token** | The frontend includes a secret key stored in `.env`. The backend verifies it on each request. | Ensures only trusted frontend clients can access the API. |
| **Serializer Validation**                  | All data passes through DRF serializers before saving.                                        | Prevents malformed or malicious data.                     |
| **CSRF & CORS Middleware**                 | Default Django middleware enabled.                                                            | Restricts cross-origin and CSRF attacks.                  |
| **Environment Variables**                  | Secrets and credentials stored in `.env`.                                                     | Protects sensitive information from exposure.             |

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

### Performance

**Lighthouse Performance Summary:**

The site has been tested using Google Lighthouse to ensure modern web quality and performance benchmarks are met. Current scores:

| Metric             |    Score |
| ------------------ | -------: |
| **Performance**    | 95 - 100 |
| **Accessibility**  |      100 |
| **Best Practices** |      100 |
| **SEO**            |      100 |

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
