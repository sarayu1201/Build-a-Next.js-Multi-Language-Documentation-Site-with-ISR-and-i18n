🧾 Docs Portal – Multi-Language Documentation Platform

Docs Portal is a high-performance, multi-language documentation system built with Next.js. It delivers a modern documentation experience using Incremental Static Regeneration (ISR), internationalization (i18n), versioned documentation, client-side search, Swagger-powered API references, theme switching, and full Docker support.

This project demonstrates how production-grade documentation portals are built for technical products, developer platforms, and enterprise knowledge bases.

🚀 Core Features

📄 Markdown-based documentation for easy content authoring

🔁 ISR-powered static pages with 60-second revalidation

🌍 Built-in internationalization (i18n) supporting:

English (en)

Spanish (es)

French (fr)

German (de)

🔀 Multiple documentation versions (v1, v2, v3)

🔍 Fast client-side full-text search

📑 Auto-generated Table of Contents (TOC) with active section highlighting

📘 API documentation rendered using Swagger UI

🌙 Light & Dark theme support

💬 Page-level feedback widget

🐳 Fully dockerized setup with Docker Compose

🛠️ Tech Stack

Framework: Next.js (App Router)

Styling: Tailwind CSS with CSS variables

Markdown Processing: remark, remark-html, remark-slug

Search: FlexSearch

API Docs: swagger-ui-react

Containerization: Docker & Docker Compose

📂 Project Structure
.
├── app/
│   ├── [lang]/docs/[version]/[slug]/page.tsx
│   ├── api-reference/page.tsx
│   └── layout.tsx
├── components/
│   ├── Header.tsx
│   ├── Sidebar.tsx
│   ├── Search.tsx
│   ├── VersionSelector.tsx
│   ├── ThemeToggle.tsx
│   ├── TableOfContents.tsx
│   └── FeedbackWidget.tsx
├── _docs/
│   ├── en/
│   ├── es/
│   ├── fr/
│   └── de/
├── public/
│   └── openapi.json
├── docker-compose.yml
├── Dockerfile
├── .env.example
├── tailwind.config.ts
└── README.md

🧪 Environment Variables

All required environment variables are documented in .env.example.

Example:

# Application environment
NODE_ENV=development

# Public Next.js variables
NEXT_PUBLIC_SITE_NAME=Docs Portal


⚠️ Security Note:
Never commit real secrets. Only use sample or placeholder values in .env.example.

🐳 Running with Docker

The application is fully containerized and can be started using Docker Compose.

🔧 Prerequisites

Docker

Docker Compose

▶️ Start the application

From the project root:

docker-compose up --build


Once the containers are running, open:

http://localhost:3000


Health checks ensure the container is marked healthy only after the app responds correctly.

🔍 API Reference

API documentation is available at:

/api-reference


Swagger UI renders the OpenAPI specification from:

public/openapi.json

🌍 Localization & Routing

Example localized documentation routes:

/en/docs/v1/introduction

/es/docs/v2/introduction

/fr/docs/v3/introduction

/de/docs/v1/introduction

Users can switch both language and documentation version directly from the UI.

📑 Incremental Static Regeneration (ISR)

All documentation pages are pre-rendered statically

Pages are revalidated every 60 seconds

Combines fast performance with up-to-date content

💬 Feedback System

Each documentation page includes a lightweight feedback component.
User responses are handled entirely on the client—no backend services required.

📦 Local Development (Without Docker)
1️⃣ Clone the repository
git clone <repository-url>
cd docs-portal

2️⃣ Install dependencies
npm install
# or
yarn install
# or
pnpm install

3️⃣ Run the development server
npm run dev
# or
yarn dev
# or
pnpm dev


Open http://localhost:3000 in your browser.

🏗️ Production Build
npm run build
npm run start


This creates an optimized production build and serves it efficiently.
