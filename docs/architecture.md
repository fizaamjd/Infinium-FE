# Architecture

Browser → lib/api/client.ts → Express API → Supabase and Python agent/model providers. lib/auth-context.tsx coordinates session state; route pages and components render account, repository, query and assistance surfaces. NEXT_PUBLIC_API_URL is a public build-time setting.

The frontend should not receive service-role credentials or provider keys. Navigation guards improve UX but are not backend authorization. Mermaid diagrams and model-provided content require safe rendering; user review remains necessary.
