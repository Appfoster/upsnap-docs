# Development Guide

This guide covers the architecture, project structure, and coding standards for the UpSnap Strapi plugin.

---

## Project Structure

```text
upsnap/
├── admin/                  # React-based Admin Panel UI
│   └── src/
│       ├── components/     # Reusable UI components (forms, tables, layouts)
│       ├── hooks/          # Custom React hooks for data fetching and state
│       ├── pages/          # Main plugin pages (Dashboard, Settings, Features)
│       ├── utils/          # Admin-side helper functions and request wrappers
│       └── index.ts        # Plugin registration and admin entry point
├── server/                 # Strapi Backend Logic (TypeScript)
│   └── src/
│       ├── bootstrap.ts    # Plugin initialization logic
│       ├── controllers/    # API controllers handling requests from admin UI
│       ├── routes/         # Definition of plugin API endpoints
│       ├── services/       # Core business logic and UpSnap.ai API communication
│       ├── content-types/  # Schema definitions for local data storage
│       └── index.ts        # Server-side entry point
├── package.json            # Plugin dependencies and build scripts
└── tsconfig.json           # TypeScript configuration
```

---

## Architecture

### Backend (Server)

The Strapi backend acts as a secure proxy between the Admin UI and the UpSnap.ai API.

- **Services:** Centralized logic for communicating with `api.upsnap.ai`. Handles authentication, data normalization, and error handling.
- **Controllers:** Bridge between API routes and services. Extract request parameters and format responses.
- **Routes:** Define internal API endpoints used by the admin panel (e.g., `/upsnap/monitors`).

---

### Frontend (Admin)

- **React & Strapi Design System:** Built using React 18 and follows Strapi Design System guidelines.
- **Custom Hooks:** Located in `admin/src/hooks` for handling data fetching, loading, and errors.
- **Modular Pages:** Each feature (Reachability, Lighthouse, etc.) is a standalone page in `admin/src/pages`.

---

## Development Workflow

### Prerequisites

- Strapi v5.x
- Node.js >= 18.x
- TypeScript knowledge

---

### Local Setup

1. Clone the repository into your Strapi project under:
   ```
   src/plugins/upsnap
   ```
   or install it as a local dependency.

2. Enable the plugin in `config/plugins.ts`:

```typescript
export default {
  upsnap: {
    enabled: true,
    resolve: './src/plugins/upsnap'
  },
};
```

3. Run Strapi with admin watch mode:

```bash
npm run develop -- --watch-admin
```

4. Open the admin panel and access **Upsnap** from the sidebar.

---

## Coding Standards

- **TypeScript:** Use strict typing across components, services, and controllers.
- **Strapi Design System:** Use `@strapi/design-system` components for UI consistency.
- **React:** Prefer functional components with hooks.

---

## Security & Validation

- **RBAC:** Ensure all controllers respect Strapi Role-Based Access Control.
- **Data Sanitization:** Validate incoming data in controllers.
- **Error Handling:** Use Strapi's built-in utilities for consistent responses.

---

## Adding a New Feature

To add a new monitoring feature:

1. **Service:** Add logic in `server/src/services`
2. **Controller:** Expose via controller method
3. **Route:** Register in `server/src/routes`
4. **Page Component:** Create UI in `admin/src/pages`
5. **Admin Registration:** Register menu/page in `admin/src/index.ts`

---

## Testing

- **UI Testing:** Check responsiveness and accessibility using Strapi components
- **API Testing:** Use Postman or Strapi Swagger plugin
- **Build Verification:**

```bash
npm run build
```

Ensure TypeScript compilation and bundling succeed.