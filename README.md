# Dynamic Routing Project

This project demonstrates dynamic routing in Astro using NPM and TypeScript.

## Project Structure

```
├── src/
│   ├── pages/
│   │   ├── index.astro
│   │   └── details/
│   │       └── [id].astro
│   ├── components/
│   └── layouts/
├── package.json
└── tsconfig.json
```

## Key Features

- **Dynamic Routing**: Implemented using Astro's file-based routing system
- **TypeScript Support**: Full TypeScript integration for better development experience

## Dynamic Routes

The project uses dynamic routing through the `/details/[id].astro` pattern. When accessing URLs like `/details/1` or `/details/2`, Astro automatically captures the ID parameter, which can be accessed using:

```typescript
const { id } = Astro.params;
```

This parameter is then used to fetch individual item data:

```typescript
const data = await fetch(`https://api.example.com/items/${id}`);
```

## Available Scripts

- **Development Server**
  ```bash
  npm run dev
  ```
  Starts the development server at `localhost:3000`

- **Production Build**
  ```bash
  npm run build
  ```
  Creates an optimized production build in the `dist` directory