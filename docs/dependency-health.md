# Dependency health

Snapshot: 2026-10-19. npm audits contact the registry and report known dependency advisories; these are not an application penetration test. Full and production-only counts are shown separately. Compatible updates were applied without force upgrades.

| Component | Full audit | Production-only audit |
| --- | --- | --- |
| Infinium-FE | 5 high, 2 low | 2 low |

Remaining high findings are in the development ESLint/braces chain. The production tree retains two low findings in Mermaid/KaTeX. The registry suggests a breaking Mermaid major upgrade and a downgrade of the framework ESLint config; neither was forced. Treat model-generated diagrams as untrusted and plan a separately validated rendering upgrade.

Recheck with npm audit and npm audit --omit=dev in the relevant package directory. Do not use npm audit fix --force merely to obtain a zero count. Source-level access controls, secret storage, workflow permissions and data retention require their own review.
