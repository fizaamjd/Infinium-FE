# Infinium-FE

![CI](https://github.com/fizaamjd/Infinium-FE/actions/workflows/ci.yml/badge.svg?branch=main)

The Next.js frontend for Infinium, a repository-aware developer assistant. It provides repository/data-source management, codebase queries, architecture diagrams, refactoring, PDF analysis, feedback and analytics views backed by the separate application API.

## Live demo video

https://github.com/user-attachments/assets/5620ed13-da0e-47b4-8b99-5827b910646f

[Video and HTML source](https://github.com/fizaamjd/Infinium/tree/evaluation-1/docs/media)

The walkthrough shows the whole Infinium product, including workflows provided by the companion services. It is a motion presentation, not a measured model benchmark.

## Run locally

Use Node.js 22 and npm with the committed lockfile.

```sh
npm ci
cp .env.local.example .env.local
npm run dev
```

Open http://localhost:3000. NEXT_PUBLIC_API_URL should point to the Express server, typically http://localhost:5000. It is embedded into the browser build; use the deployed API origin when building for production. The Express server must permit the frontend origin through CORS.

## Main surfaces

| Area | Routes |
| --- | --- |
| Accounts | /auth, /auth/callback, /onBoarding |
| Repository workflow | /repositories, /datasources, /query |
| Code assistance | /reasoning, /architecture, /code-refactor, /pdf |
| Review and reporting | /dashboard, /analytics, /decision-history, /feedback, /error-insights |

These are interface surfaces; service availability, access checks and model results depend on the backend services. Session tokens are stored in browser localStorage. Avoid sensitive code on untrusted browsers.

## Validation

npm run typecheck and npm run build are required CI gates. Strict npm run lint is documented separately so inherited lint debt is visible rather than silently ignored. CI does not provision accounts, run model generation, or verify every UI flow. See [testing](docs/testing.md).

## System repositories

| Repository | Responsibility |
| --- | --- |
| [Infinium](https://github.com/fizaamjd/Infinium) | Python RAG agent, ingestion, retrieval, integrations and VS Code extension |
| [Infinium-BE](https://github.com/fizaamjd/Infinium-BE) | Express application API, Supabase persistence, auth and service orchestration |
| [Infinium-FE](https://github.com/fizaamjd/Infinium-FE) | Next.js user interface |

## Maintenance status

See [verification](docs/verification.md) for checks actually run and [dependency health](docs/dependency-health.md) for remaining findings.

## Contributing and maintenance

[Contributing](CONTRIBUTING.md) · [Support](SUPPORT.md) · [Security](SECURITY.md) · [Code of conduct](CODE_OF_CONDUCT.md) · [Changelog](CHANGELOG.md)

## License

[MIT](LICENSE) for original contributions the maintainer is authorized to license. Third-party and collaborator rights remain separate; see [license scope](docs/license-scope.md).
