# 📘 Docs Portal – Multi-Language Documentation Platform

A high-performance, multi-language documentation portal built with **Next.js**, featuring **Incremental Static Regeneration (ISR)**, **internationalization**, **versioned documentation**, **full-text search**, **API reference using Swagger UI**, **dark/light theme**, and **Dockerized deployment**.

This project demonstrates modern documentation architecture commonly used in real-world product documentation and knowledge bases.

---

## 🚀 Features

- 📄 **Markdown-based documentation system**
- 🔁 **Incremental Static Regeneration (ISR)** with 60s revalidation
- 🌍 **Internationalization (i18n)**
  - English (en)
  - Spanish (es)
  - French (fr)
  - German (de)
- 🔀 **Versioned documentation** (v1, v2, v3)
- 🔍 **Client-side full-text search**
- 📑 **Auto-generated Table of Contents (TOC)** with active section tracking
- 📘 **API Reference** rendered using Swagger UI
- 🌙 **Light / Dark theme toggle**
- 💬 **Feedback widget** on each documentation page
- 🐳 **Fully containerized** with Docker & Docker Compose

---

## 🛠️ Tech Stack

- **Framework:** Next.js (App Router)
- **Styling:** Tailwind CSS + CSS Variables
- **Markdown Processing:** remark, remark-html, remark-slug
- **Search:** FlexSearch
- **API Docs:** swagger-ui-react
- **Containerization:** Docker, Docker Compose

---

## 📂 Project Structure

```
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
```

---

## 🧪 Environment Variables

All required environment variables are documented in **`.env.example`**.

Example:

```env
# Application environment
NODE_ENV=development

# Next.js public variables
NEXT_PUBLIC_SITE_NAME=Docs Portal
```

> ⚠️ **Do not commit real secrets.**  
> Only example or placeholder values should be included.

---

## 🐳 Docker Setup (Required)

The application is fully containerized and can be started using Docker Compose.

### 🔧 Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

### ▶️ Run the Application

From the project root:

```bash
docker-compose up --build
```

The application will be available at:

```
http://localhost:3000
```

Docker health checks ensure the app is running correctly before marking the container as healthy.

---

## 🔍 API Reference

The API documentation is available at:

```
/api-reference
```

It is rendered using **Swagger UI** from the OpenAPI specification located at:

```
public/openapi.json
```

---

## 🌍 Internationalized Routes

Examples:

- `/en/docs/v1/introduction`
- `/es/docs/v2/introduction`
- `/fr/docs/v3/introduction`
- `/de/docs/v1/introduction`

Language and version can be switched using the UI controls.

---

## 📑 Incremental Static Regeneration (ISR)

- All documentation pages are **statically generated**
- Pages are **revalidated every 60 seconds**
- Ensures **fast performance** with **fresh content**

---

## 💬 Feedback Widget

Each documentation page includes a feedback form where users can submit feedback.  
No backend is required; submission confirmation is handled client-side.

---

## 📦 Installation & Development

If you want to run the project locally without Docker:

### 1. Clone the repository

```bash
git clone <repository-url>
cd docs-portal
```

### 2. Install dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

### 3. Run the development server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🏗️ Build for Production

```bash
npm run build
npm run start
```
---