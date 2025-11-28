# Cloudflare Pages Deployment with Wrangler

This project is configured for deployment to Cloudflare Pages using Wrangler CLI.

## Prerequisites

1. Install Wrangler globally (recommended):
```bash
npm install -g wrangler
```

2. Login to Cloudflare:
```bash
wrangler login
```

## Deployment Methods

### Method 1: Using Wrangler CLI (Direct Deploy)

1. **Build the project:**
```bash
npm run build
```

2. **Deploy to Cloudflare Pages:**
```bash
wrangler pages deploy out --project-name=test-fe
```

3. Your app will be deployed and you'll get a URL like: `https://test-fe.pages.dev`

### Method 2: Using npm Scripts

Deploy with a single command:
```bash
npm run pages:deploy
```

### Method 3: GitHub Integration

1. Push your code to a GitHub repository
2. Go to Cloudflare Pages dashboard
3. Click "Create a project"
4. Connect your GitHub repository
5. Configure build settings:
   - **Build command:** `npm run build`
   - **Build output directory:** `out`
   - **Node version:** 18 or higher
6. Click "Save and Deploy"

## Configuration Files

- `wrangler.toml` - Wrangler configuration
- `.node-version` - Specifies Node.js version
- `next.config.ts` - Next.js configured for static export

## Local Development

Run the development server:
```bash
npm run dev
```

## Environment Variables

No environment variables are required for this basic setup.

## Updating the Deployment

To update your deployed app:
```bash
npm run build
wrangler pages deploy out --project-name=test-fe
```

Or use the npm script:
```bash
npm run pages:deploy
```
