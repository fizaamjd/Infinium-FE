# Testing

```sh
npm ci
npm run typecheck
npm run build
python3 scripts/check-docs.py
# npm run lint is an additional strict diagnostic; see docs/testing.md.
```

CI runs without production credentials or real account data. Its scope is limited to the checks named in the workflow, not end-to-end production validation. A passing workflow is not a security audit, retrieval benchmark, native extension runtime test, or service uptime guarantee.

Verification results and remaining lint/dependency findings are recorded in [verification](verification.md).
