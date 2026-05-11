---
"@googleworkspace/cli": minor
---

Re-enable domain-wide delegation for service-account credentials via the
`GOOGLE_WORKSPACE_CLI_IMPERSONATED_USER` environment variable. When set, its
value is passed as the JWT `subject` to impersonate that user. No CLI flags
are added; the variable is ignored for user credentials.

The service-account token cache is now keyed per identity
(`sa_<hash>_token_cache.json`), so switching between SA keys or impersonated
users no longer reuses a stale token from a previous identity.
