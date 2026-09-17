# TWE Deployment

## Target environment

TWE production is designed for cPanel/shared hosting. The deployed package must not depend on running Composer or npm on the production server.

## Pre-deployment

1. Pull the intended commit from `main`.
2. Confirm `.env` is not present in the repository/package.
3. Run PHP syntax checks.
4. Review any database migrations.
5. Verify required environment variables are represented in `.env.example`.
6. Build frontend dependencies before packaging if a build system is introduced.
7. Package without local caches, logs, `.git`, credentials or production database dumps.

## Deployment

1. Back up the current application and database.
2. Upload/extract the release package.
3. Preserve or recreate the server-side `.env`.
4. Apply documented migrations.
5. Verify writable runtime directories.
6. Clear runtime caches where appropriate.
7. Run health checks.

## Health checks

Verify homepage, article pages, tools, search, authentication, Control Centre permissions, email delivery, payment configuration, Valron lead handoff and mobile navigation.

Production errors must never expose stack traces or secrets.
