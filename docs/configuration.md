# Configuration

NEXT_PUBLIC_API_URL is the only application API setting read by lib/api/client.ts. It must point to the Express service origin, without a trailing API path; for example http://localhost:5000. NEXT_PUBLIC values are embedded into the public browser build. Never put OAuth client secrets, service-role keys or model keys here.

For Vercel, configure the production value before building and permit the deployed frontend origin in Infinium-BE's ALLOWED_ORIGINS. A successful static build does not check connectivity or authentication against that server.
