# OGA: rules for the AI

OGA is a platform where experienced African developers (the Oga) give tasks to apprentices.
We are beginners: explain everything in simple French.

## Licences (CADEV rules, article 6)

- Allowed: MIT, Apache-2.0, BSD-2/3, ISC. Forbidden: GPL, AGPL, LGPL, SSPL.
- Check a dependency's licence before adding it. Never add a library without asking.
- Never use PM2 (AGPL). Use systemd.

## Security

- No secrets in code: passwords and keys go in `.env`, never committed.
- Passwords hashed with Argon2id, never shown or logged.
- All user input is validated on the server with zod.
- Database access only through Prisma, never SQL built by string concatenation.
- OGA never runs apprentices' code: static analysis only.
- GitHub webhooks are rejected (401) if the HMAC-SHA256 signature is invalid.
- Amounts are integers in FCFA, never decimals.

## AI

- Everything the AI writes or changes is declared in `IA.md`.
- Nobody merges code they cannot explain.

## Teamwork

- Never work directly on `main`. One branch per task, one PR, one approval.
- Squash and merge only.
