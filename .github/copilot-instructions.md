# GitHub Copilot Project Instructions

## Project Overview
This is an Astro project that uses React components and TailwindCSS for styling. When making suggestions, please consider the following framework-specific details and conventions.

## Tech Stack
- Astro v5.x
- React as UI library
- TailwindCSS for styling (v4.x)
- TypeScript for type safety

## Project Structure
```
├── src/
│   ├── components/     # React and Astro components
│   ├── layouts/        # Astro layout components
│   ├── pages/          # Astro pages and routes
│   ├── styles/         # Global styles
│   └── utils/          # Utility functions
├── public/            # Static assets
└── astro.config.mjs   # Astro configuration
```

## Component Conventions

### Astro Components
- Use `.astro` extension
- Follow kebab-case for filenames
- Example structure:

```astro
---
// Imports and props
interface Props {
  title: string;
}

const { title } = Astro.props;
---

<div class="component-wrapper">
  <h1>{title}</h1>
  <slot />
</div>

<style>
  /* Scoped styles if needed */
</style>
```

### React Components
- Use `.tsx` extension
- Follow PascalCase for component names and files
- Prefer functional components with hooks
- Example structure:

```tsx
import type { FC } from 'react';
import { useState } from 'react';

interface ComponentProps {
  title: string;
}

export const MyComponent: FC<ComponentProps> = ({ title }) => {
  const [state, setState] = useState('');

  return (
    <div className="component-wrapper">
      <h1>{title}</h1>
    </div>
  );
};
```

## Styling Conventions with TailwindCSS

### Base Guidelines
- Use TailwindCSS utility classes for styling
- Follow mobile-first responsive design
- Use semantic class names when creating components

### Class Order Preferences
1. Layout Properties (display, position)
2. Box Model (width, height, padding, margin)
3. Visual Properties (background, border)
4. Typography
5. Other Properties

Example:
```tsx
<div className="flex items-center justify-between w-full p-4 mb-6 bg-white rounded-lg shadow-md">
```

### Common Utility Patterns
```tsx
// Container patterns
"container mx-auto px-4"

// Flex layouts
"flex items-center justify-between"

// Grid layouts
"grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4"

// Typography
"text-base font-medium text-gray-900"

// Interactive elements
"hover:bg-blue-600 transition-colors duration-200"
```

## Type Safety
- Always use TypeScript types/interfaces for props
- Prefer explicit type annotations over inference
- Use `type` for simple types and `interface` for objects that might be extended

```typescript
interface BaseProps {
  className?: string;
}

interface ButtonProps extends BaseProps {
  variant: 'primary' | 'secondary';
  onClick: () => void;
}
```

## Best Practices

### Astro-Specific
- Use `.astro` components for pages and layouts
- Leverage Astro's partial hydration with client directives
- Use `client:*` directives appropriately for React components

### React-Specific
- Keep components small and focused
- Use custom hooks for reusable logic
- Follow React's naming conventions for hooks (use`use` prefix)

### Performance
- Prefer static routes where possible
- Use image optimization through Astro's built-in support
- Implement lazy loading for heavy components

## Common Patterns

### Layout Components
```astro
---
import Header from '../components/Header.astro';
import Footer from '../components/Footer.astro';

interface Props {
  title: string;
}

const { title } = Astro.props;
---

<!DOCTYPE html>
<html lang="en">
  <head>
    <title>{title}</title>
  </head>
  <body>
    <Header />
    <main>
      <slot />
    </main>
    <Footer />
  </body>
</html>
```

### React Components with TailwindCSS
```tsx
import type { FC } from 'react';

interface CardProps {
  title: string;
  description: string;
}

export const Card: FC<CardProps> = ({ title, description }) => {
  return (
    <div className="p-6 bg-white rounded-lg shadow-md hover:shadow-lg transition-shadow duration-300">
      <h2 className="text-xl font-bold text-gray-900 mb-2">{title}</h2>
      <p className="text-gray-600">{description}</p>
    </div>
  );
};
```

## API Integration
When suggesting API integration code, prefer using Astro's built-in fetch capabilities in `.astro` files:

```astro
---
const data = await fetch('https://api.example.com/data').then(r => r.json());
---
```

For React components that need data fetching, suggest using React Query or SWR patterns.