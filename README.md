# Déplacé Maison — E-commerce Experience

> A premium, responsive e-commerce experience engineered by **Théo** — [@onllytap](https://github.com/onllytap).

This project showcases my approach to building polished fullstack web applications: an immersive storefront, smooth interactions, secure authentication, persistent shopping state, online payments, and order management brought together in a cohesive user experience.

## Overview

Déplacé Maison is a fashion e-commerce application built with Next.js and React. Beyond the storefront itself, the project explores the complete customer journey—from discovering a product to authentication, checkout, payment confirmation, and order history.

### Highlights

- Responsive storefront designed for desktop and mobile
- Dynamic product catalogue and individual product pages
- Persistent shopping cart powered by Context API and local storage
- Google authentication with NextAuth
- Stripe Checkout integration and webhook-based payment processing
- Firebase-backed product and order data
- Customer order history
- Fluid animations with Framer Motion and GSAP
- Supporting pages for contact, FAQ, returns, privacy, and terms
- Custom 404 and payment status experiences

## Tech Stack

| Area | Technologies |
| --- | --- |
| Frontend | Next.js 12, React 17, Styled Components |
| Interactions | Framer Motion, GSAP, React Easy Marquee |
| Authentication | NextAuth.js, Google OAuth |
| Payments | Stripe Checkout, Stripe webhooks |
| Data | Firebase Firestore, Firebase Admin |
| State & networking | React Context API, localStorage, Axios |

## Architecture

The application uses Next.js pages for both the user interface and server-side endpoints. Stripe Checkout handles the payment flow, while a signed webhook records completed orders through Firebase Admin. NextAuth provides Google authentication, and client-side cart state persists between sessions through local storage.

```text
Customer interface (Next.js / React)
        │
        ├── NextAuth ─────────────── Google OAuth
        ├── Checkout API ─────────── Stripe Checkout
        ├── Stripe webhook ───────── Firebase order storage
        └── Firestore ────────────── Products and customer orders
```

## Getting Started

### Prerequisites

- Node.js 16+
- npm
- A Stripe account
- A Firebase project with Firestore enabled
- Google OAuth credentials

### Installation

```bash
git clone https://github.com/onllytap/deplace-maison-ecommerce-webapp.git
cd deplace-maison-ecommerce-webapp
npm install
```

Create a `.env.local` file at the root of the project:

```env
STRIPE_PUBLIC_KEY=
STRIPE_SECRET_KEY=
STRIPE_SIGNING_SECRET=

HOST=http://localhost:3000

FIREBASE_SERVICE_ACC_KEY=

GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
SECRET=
```

Never commit `.env.local` or production secrets. For `FIREBASE_SERVICE_ACC_KEY`, provide the service-account JSON in the format expected by the server environment.

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production build

```bash
npm run build
npm start
```

## What I Focused On

- Structuring a complete e-commerce journey rather than an isolated UI
- Connecting frontend interactions to authentication, payment, and data services
- Keeping payment secrets and privileged Firebase operations server-side
- Building reusable React components and consistent responsive layouts
- Creating motion and visual feedback without sacrificing usability

## Roadmap

- Migrate the application to the latest stable Next.js architecture
- Strengthen runtime validation and error handling
- Add automated unit, integration, and end-to-end tests
- Improve accessibility and performance metrics
- Add richer page transitions and theme support

## Author

**Théo — Fullstack Developer**

I build modern, typed, and scalable web applications. Based in Chartres, France, I focus on performant SaaS products, professional web platforms, application security, and highly interactive frontend experiences. My long-term goal is to bridge robust web engineering with artificial intelligence.

- GitHub: [@onllytap](https://github.com/onllytap)
- Location: Chartres, France 🇫🇷
- Core interests: Fullstack development, application security, and AI-powered products
- Preferred stack: Next.js, TypeScript, Tailwind CSS, Node.js, PostgreSQL, and Prisma

## Project Notice

This is an independent, non-commercial portfolio implementation inspired by the public Déplacé Maison storefront. Déplacé Maison remains the owner of its brand, product imagery, typography, and other original visual assets. This repository is not affiliated with or endorsed by the brand.

---

Designed and engineered as a portfolio project by **Théo** — [github.com/onllytap](https://github.com/onllytap).
