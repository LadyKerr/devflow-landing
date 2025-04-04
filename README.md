# DevFlow Landing Page

A modern landing page for DevFlow - the serverless API platform that helps developers build and deploy APIs quickly and efficiently.

## 🚀 Project Overview

DevFlow's landing page is built with modern web technologies to showcase our platform's features and capabilities. The site is built with Astro and uses React components with TailwindCSS for styling.

## 🛠️ Tech Stack

- [Astro](https://astro.build) v5.x - Static site generator
- [React](https://reactjs.org) - UI components
- [TailwindCSS](https://tailwindcss.com) v4.x - Styling
- TypeScript - Type safety

## 📁 Project Structure

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── assets/
│   │   ├── astro.svg
│   │   ├── background.svg
│   │   └── dashboard-preview.png
│   ├── components/
│   │   ├── ApiDevelopment.astro
│   │   ├── ByDevelopers.astro
│   │   ├── CallToAction.astro
│   │   ├── DashboardManagement.astro
│   │   ├── Footer.astro
│   │   ├── Hero.astro
│   │   ├── Navbar.astro
│   │   ├── TrustedByDevs.astro
│   │   └── TryYourself.astro
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

## 📋 Features

- Modern, responsive design
- Server-side rendered pages for optimal performance
- Interactive code examples
- Mobile-first approach
- TypeScript support
- TailwindCSS for styling

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |

## 🚀 Quick Start

1. Clone the repository:
```bash
git clone https://github.com/your-username/devflow-landing.git
```

2. Install dependencies:
```bash
cd devflow-landing
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and visit `http://localhost:4321`

## 💻 Development

The project follows a component-based architecture using Astro components. Key sections of the landing page include:

- Hero section with interactive code preview
- Features showcase
- API development examples
- Dashboard preview
- Testimonials
- Interactive demo section
- Call-to-action sections
- Footer with documentation and community links

## 📝 License

MIT License - see the [LICENSE](LICENSE) file for details
