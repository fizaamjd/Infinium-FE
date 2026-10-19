# Security policy

## Reporting

Use [GitHub private reporting](https://github.com/fizaamjd/Infinium-FE/security/advisories/new). Include the affected branch/commit, reproduction with synthetic data, impact and suggested mitigation. Do not post credentials, customer data, private repository contents, or real email in an issue. If a credential was exposed, revoke it through its provider; removing a file does not invalidate a token or erase earlier commits.

The maintained branch is `main`; there is no separate security support promise for old phase branches or tags. Dependency updates and CI checks do not establish a completed security audit.

## Known boundaries

- Browser auth stores the session token in localStorage; review XSS and session-management risks before handling private code.
- NEXT_PUBLIC_API_URL is public configuration, never a secret. Supabase service-role keys, GitHub secrets and model keys belong in server components/services outside this repository.
- UI routes and screenshots do not prove backend authorization, correct model answers or isolation. Account, upload and repository operations require the separate Express and Python services.

Use dedicated development services and explicit secrets. Review provider permissions, public network exposure, data retention, and deployment access before using private data. No penetration test or production-readiness certification is claimed.
