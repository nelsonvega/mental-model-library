---
noteId: "501d2cc0441411f1b4ca9109afb55b6e"
tags: []

---

<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# turn this into a structured “pre‑launch security checklist”

Here’s a structured pre‑launch security checklist tailored to a React + Supabase SaaS. You can drop this into your repo as a living doc.

***

## 1. Authentication \& Sessions

- [ ] Email verification is required for all new accounts.
- [ ] Password policy set (12+ chars, complexity, or passwordless/magic links).
- [ ] OAuth / SSO providers configured with restricted, trusted redirect URLs only.
- [ ] Using managed auth (e.g., Supabase Auth) rather than custom password storage.
- [ ] Access/refresh tokens are not stored long‑term in localStorage.
- [ ] If using cookies for auth, they are httpOnly, secure, and have SameSite set.
- [ ] Token lifetimes are short and refresh flow is implemented.
- [ ] Forced logout on password change or credential rotation is implemented.
- [ ] Rate limiting is applied on login, signup, and password reset endpoints.

***

## 2. Database \& RLS (Supabase)

- [ ] Row Level Security (RLS) is enabled on all tables that store user or tenant data.
- [ ] RLS policies enforce tenant isolation (e.g., tenant_id = auth.jwt().tenant_id).
- [ ] RLS policies enforce user ownership where needed (e.g., owner_id = auth.uid()).
- [ ] No “allow all” or overly broad RLS policies exist in production.
- [ ] All RLS policies have been tested with multiple users and tenants (happy path + abuse scenarios).
- [ ] Public or anon‑accessible tables are explicitly intended and contain only non‑sensitive data.

***

## 3. Supabase Keys, Functions, and Storage

- [ ] service_role key is used only in secure server environments (never in React/browser).
- [ ] anon key used in React is limited by strong RLS policies.
- [ ] All keys and secrets are stored in environment variables, not in source control.
- [ ] Separate Supabase projects (and keys) exist for dev, staging, and prod.
- [ ] Storage buckets are configured with appropriate privacy (private vs public).
- [ ] Bucket policies restrict read/write to the correct user/tenant only.
- [ ] Edge Functions / RPCs check auth (JWT) and enforce authorization on every request.
- [ ] Rate limiting is applied on Edge Functions / RPC endpoints handling sensitive operations.

***

## 4. React Frontend Security

- [ ] No secrets or service_role keys are present in the frontend bundle.
- [ ] All user inputs are validated client‑side for UX, and server‑side for security.
- [ ] No raw SQL strings are constructed in the frontend; only parameterized Supabase calls.
- [ ] No unsafe HTML injection (dangerouslySetInnerHTML) without strict sanitization and necessity.
- [ ] Error messages shown to users are generic and do not expose stack traces or SQL.
- [ ] Detailed errors are logged only on the server / logging system, not exposed to the client.

***

## 5. HTTP, CORS, and Browser Protections

- [ ] CORS configuration allows only trusted production and staging domains (no wildcard in prod).
- [ ] HTTPS is enforced across all environments (no plain HTTP endpoints in production).
- [ ] Security headers configured (at CDN/host or edge):
    - [ ] Content‑Security‑Policy (CSP) in place and tested.
    - [ ] X‑Frame‑Options / frame‑ancestors prevent clickjacking (e.g., DENY or sameorigin).
    - [ ] Referrer‑Policy is set appropriately (e.g., strict‑origin‑when‑cross‑origin).
    - [ ] X‑Content‑Type‑Options, X‑XSS‑Protection (if applicable) configured.
- [ ] Cookies (if used) have secure and SameSite flags configured correctly.

***

## 6. Monitoring, Logging, and Backups

- [ ] Application logs capture key security events (logins, password resets, role changes, key rotations).
- [ ] Supabase logs (auth, DB, storage) are enabled and retained for an appropriate duration.
- [ ] Alerts or reviews are set up for unusual auth failures, sudden traffic spikes, or rate‑limit hits.
- [ ] Automated database backups are enabled for production.
- [ ] A recent backup has been successfully restored into a non‑prod environment as a test.

***

## 7. Dependencies, Environments, and Build Pipeline

- [ ] React, Supabase client, and major dependencies are on maintained, non‑vulnerable versions.
- [ ] A dependency scanning tool (e.g., Snyk, Dependabot) is configured and monitored.
- [ ] Dev, staging, and prod have separate databases, auth configs, and keys.
- [ ] No real production PII is used in dev/staging environments.
- [ ] Build pipelines do not print secrets to logs and restrict access to env vars to necessary steps only.

***

## 8. Threat Modeling \& Incident Response

- [ ] Data‑flow diagram exists showing React → Supabase → external services and where data is stored.
- [ ] Major threat scenarios are documented (e.g., stolen JWT, leaked anon key, compromised account).
- [ ] Mitigations for each major threat are identified (RLS, rate limits, MFA, alerts, etc.).
- [ ] There is a written incident response plan including:
    - [ ] How to detect an incident (signals, dashboards, logs).
    - [ ] How to contain (key rotation, forced logouts, blocking tenants/users).
    - [ ] How to communicate with affected customers and regulators if needed.
    - [ ] How to run a post‑mortem and implement follow‑up fixes.

***

## 9. Final Pre‑Launch Review

- [ ] Security checklist has been reviewed and signed off by at least one other person.
- [ ] A security “smoke test” has been done from an attacker’s perspective (try to break RLS, access other tenant data, abuse APIs).
- [ ] A schedule exists for recurring security reviews (e.g., quarterly or before major releases).

***

If you want a version formatted specifically for GitHub (with sections collapsed, owner columns, and severity tags), I can reshape this into a checklist template with owners and due dates.

