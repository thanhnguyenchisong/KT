# Knowledge Transfer Handover Acceptance Checklist

> **Goal**: Confirm that the new developer/team has actually received, verified, and can independently use the source code, access, documentation, operational knowledge, and ownership required to maintain the application.

---

## 0.1 Source Code Transfer

- [ ] All source code repositories listed by name and URL
- [ ] Frontend repository received and cloned
- [ ] Backend repository received and cloned
- [ ] Shared library/common module repositories received
- [ ] Infrastructure-as-code repository received, if any
- [ ] Deployment scripts repository received, if any
- [ ] Documentation repository or wiki access received
- [ ] Correct production branch identified
- [ ] Latest production tag/commit SHA identified
- [ ] **Production artifact verified to match a known repo commit** (deployed image tag/JAR matches source)
- [ ] Current development branch identified
- [ ] In-flight work identified: open PRs, unreleased hotfixes, half-merged feature branches
- [ ] Repository access tested by cloning locally
- [ ] Permission to create branch confirmed and tested
- [ ] Permission to push branch confirmed and tested
- [ ] Permission to create PR/MR confirmed and tested
- [ ] Repo admin/maintainer ownership transferred, if required
- [ ] Git LFS configured, if the repo uses large binary assets
- [ ] Private npm registry access received and tested, if applicable
- [ ] Private Maven/Gradle repository (Nexus, Artifactory) access received and tested, if applicable

## 0.2 Application Access

- [ ] Local environment setup instructions received
- [ ] Dev environment URL received and login tested
- [ ] QA/UAT/staging environment URL received and login tested
- [ ] Pre-production environment URL received and login tested, if any
- [ ] Production environment URL received
- [ ] Test user accounts received with credentials
- [ ] Admin user account received, if applicable
- [ ] Role/permission matrix received (which role can do what)
- [ ] VPN access received and connection tested
- [ ] SSO access received and login tested
- [ ] Firewall/IP allowlist access confirmed, if required
- [ ] Cloud IAM roles/permissions granted (specific policies, not just console access)
- [ ] Third-party service accounts received:
  - [ ] Email service (SendGrid, SES, etc.)
  - [ ] SMS/notification service
  - [ ] Payment gateway, if applicable
  - [ ] External API accounts with credentials
  - [ ] Any other SaaS/vendor portals

## 0.3 Build And Run Verification

- [ ] Required Java version confirmed (exact version, e.g., JDK 17.0.x)
- [ ] Required Node.js version confirmed (exact version, e.g., 18.x)
- [ ] Required Angular version confirmed (exact version, e.g., 16.x)
- [ ] Required Maven/Gradle version confirmed
- [ ] Required npm/yarn/pnpm version confirmed
- [ ] Docker and Docker Compose installed and working
- [ ] `docker-compose.yml` or equivalent received and reviewed
- [ ] Local infrastructure dependencies documented and running:
  - [ ] Database container or local instance
  - [ ] Redis/cache container, if required
  - [ ] Kafka/RabbitMQ/message broker container, if required
  - [ ] Elasticsearch/search engine container, if required
  - [ ] Any other local service dependencies
- [ ] Backend builds successfully on local machine
- [ ] Frontend builds successfully on local machine
- [ ] Backend runs locally
- [ ] Frontend runs locally
- [ ] Frontend can call backend locally (proxy/CORS working)
- [ ] Unit tests can run locally and pass
- [ ] Integration tests can run locally, if available
- [ ] E2E tests can run locally, if available
- [ ] Required environment variables documented with example values
- [ ] Required config files/templates received (`.env.example`, `application-local.yml`, etc.)
- [ ] Required local certificates received, if any
- [ ] "Clean machine to running app" guide written and verified

## 0.4 Database And Data

- [ ] Database engine and exact version confirmed (e.g., PostgreSQL 15.3)
- [ ] Database schema received
- [ ] Migration tool identified (Flyway, Liquibase) and migration files received
- [ ] How to create and apply a new migration documented
- [ ] Seed/reference data received
- [ ] ERD or schema documentation received
- [ ] Dev database access tested: can connect via CLI/IDE, run a SELECT, see expected tables
- [ ] Staging/UAT database access tested: same verification as dev
- [ ] Production database access policy clarified (read-only? bastion host? approval needed?)
- [ ] Production data volume documented (approximate size in GB, row counts for large tables)
- [ ] Stored procedures, triggers, views, and functions documented, if any
- [ ] Database connection pool configuration documented (HikariCP settings, max connections)
- [ ] High-write tables vs. read-heavy tables identified
- [ ] Indexes documented with their purpose
- [ ] Soft delete vs. hard delete approach documented
- [ ] Known data integrity issues documented (orphaned records, constraint violations)
- [ ] Database user accounts listed; old team credentials scheduled for rotation
- [ ] Backup process documented with schedule and retention
- [ ] Restore process documented and tested (or at minimum, walked through)
- [ ] Data masking/anonymization process for non-prod environments documented
- [ ] Sensitive/PII data locations documented

## 0.5 Deployment And Operations

- [ ] CI/CD system access received and login tested
- [ ] Pipeline configuration file location identified (Jenkinsfile, `.github/workflows/`, etc.)
- [ ] Pipeline stages documented (build, test, lint, scan, package, deploy)
- [ ] Build artifact registry access received and tested
- [ ] Docker/container registry access received and tested, if applicable
- [ ] Cloud console access received with specific IAM permissions verified
- [ ] Kubernetes/hosting platform access received and tested (`kubectl get pods` works), if applicable
- [ ] Deployment process documented as step-by-step runbook for each environment
- [ ] Deployment order/dependencies documented (e.g., DB migration before backend, backend before frontend)
- [ ] Environment-specific configuration differences documented (what differs between dev/staging/prod)
- [ ] Deployment strategy documented (rolling update, blue/green, canary)
- [ ] Developer has deployed to dev environment independently
- [ ] Developer has deployed to staging/UAT environment independently
- [ ] Production deployment approval process documented (who approves, what gates exist)
- [ ] **Rollback procedure documented AND rehearsed on staging**
- [ ] Health check endpoints documented with expected responses
- [ ] Smoke test checklist received (automated or manual)
- [ ] Scheduled maintenance windows documented
- [ ] Upcoming planned events documented (customer go-lives, migrations, etc.)

## 0.6 Monitoring And Support

- [ ] Application logs access received and verified (can search and find a specific request)
- [ ] Production logs access policy clarified
- [ ] Example log queries provided for common troubleshooting scenarios
- [ ] Structured logging key fields documented (correlation ID, user ID, request ID)
- [ ] Monitoring dashboard access received and key dashboards identified
- [ ] SLA/SLO targets documented (response time P95, error rate threshold, uptime %)
- [ ] Key metrics explained: what "healthy" looks like numerically
- [ ] Alerting tool access received and alert rules reviewed
- [ ] Error tracking tool access received, if any (Sentry, Bugsnag, etc.)
- [ ] Top 10 common production issues documented with symptoms, root cause, and resolution steps
- [ ] Incident escalation path received with names, roles, and contact methods
- [ ] On-call process documented (rotation, response SLA per severity)
- [ ] Support contact list received (business, infra, security, QA, vendor contacts)
- [ ] Support ticket history reviewed (what do users actually complain about)
- [ ] Last 6-12 months of incident history received with root causes and fixes

## 0.7 Security And Secrets

- [ ] Secret manager access received and verified (can list, read, and if authorized, rotate)
- [ ] Location of all secrets documented (which secrets, which manager, which environment)
- [ ] Secret rotation process documented with schedule
- [ ] API keys ownership clarified and transferred to incoming team accounts
- [ ] OAuth/SSO client configuration documented
- [ ] SSL/TLS certificate ownership clarified
- [ ] **SSL/TLS certificate expiry dates documented with renewal owners assigned**
- [ ] Domain/DNS ownership clarified
- [ ] CORS configuration documented
- [ ] Rate limiting configuration documented
- [ ] WAF rules documented, if applicable
- [ ] Security scan process documented (SAST, DAST, dependency scanning)
- [ ] Penetration test results reviewed, if available
- [ ] Known vulnerabilities reviewed with remediation status
- [ ] No secrets are hardcoded in source code (verified by scan)
- [ ] Compliance requirements documented (GDPR, HIPAA, PCI-DSS, etc.)
- [ ] **Outgoing team access revocation plan with timeline**

## 0.8 Business And Product Knowledge

- [ ] Business purpose of the application explained and incoming developer can explain it back
- [ ] Main users and roles understood (incoming developer can list them)
- [ ] SLA commitments to customers/stakeholders documented
- [ ] Top 5 user journeys walked through end-to-end (UI to API to DB and back)
- [ ] Top 3 complex business flows walked through with code
- [ ] Current backlog reviewed
- [ ] In-progress work reviewed and status documented
- [ ] Known bugs reviewed with workarounds
- [ ] Technical debt inventory reviewed with priority ranking
- [ ] Upcoming roadmap reviewed for next 1-2 quarters
- [ ] Business owner/contact identified with communication channel
- [ ] Peak usage periods documented (time of day, end of month, seasonal)

## 0.9 Ownership Transfer

- [ ] Code repository ownership transferred (admin rights)
- [ ] CI/CD pipeline ownership transferred
- [ ] Deployment ownership transferred
- [ ] Monitoring and alerting ownership transferred
- [ ] Incident response ownership transferred
- [ ] Vendor/service account ownership transferred, if applicable
- [ ] Domain/DNS ownership transferred, if applicable
- [ ] Cloud/resource billing owner identified and documented
- [ ] **Monthly infrastructure cost documented and budget alerts configured**
- [ ] Auto-scaling configuration and resource limits documented
- [ ] License/subscription renewal dates and owners documented
- [ ] **Third-party service billing transferred to incoming team accounts**
- [ ] Transition/shadow period agreed (2-4 weeks of parallel operation recommended)
- [ ] Post-handover support agreement documented: duration, response SLA, escalation channel
- [ ] Knowledge escrow plan: what happens if outgoing team becomes unreachable
- [ ] Final KT sign-off date agreed

## 0.10 Final Acceptance Criteria

### Mandatory (all must pass before sign-off)

- [ ] Production artifact verified to match a known repo commit
- [ ] Developer set up the full project on a clean machine without assistance
- [ ] Developer ran all test suites (unit, integration, E2E) and can interpret results
- [ ] Developer made a code change and deployed it to dev/staging independently
- [ ] Developer performed a rollback on staging successfully
- [ ] Developer investigated a real past production issue from logs to root cause without help
- [ ] Developer can draw the system architecture from memory and explain data flow
- [ ] Developer can list all external integrations, their owners, and fallback behavior
- [ ] All secrets are accessible to incoming team and not hardcoded
- [ ] Outgoing team access revocation schedule is documented and agreed
- [ ] Post-handover support window is documented: duration, SLA, escalation channel
- [ ] Third-party service accounts transferred or billing ownership clarified
- [ ] Certificate and license expiry calendar created with renewal owners assigned
- [ ] Both teams sign the handover acceptance document with date

### Recommended (complete within 2 weeks post-handover)

- [ ] Developer handled a real production alert or incident (shadowed or solo)
- [ ] Developer performed a production deployment following the full release process
- [ ] Developer onboarded another team member using the documentation created during KT
- [ ] Developer wrote or updated at least one runbook based on real operational experience

---

## Red Flags — Do Not Accept Handover If

| Red Flag | Risk | Action |
|---|---|---|
| Production code doesn't match any repo commit | You don't own what's running | Block sign-off until verified |
| Rollback procedure exists only on paper | First real rollback will fail | Rehearse on staging before accepting |
| Secrets are hardcoded or in shared docs | Security breach risk | Escalate to security team immediately |
| Outgoing team has no access revocation plan | Unknown actors with production access | Block sign-off until plan exists |
| Third-party billing on outgoing team's credit card | Services will stop when card expires | Transfer billing before accepting |
| No monitoring or alerting | Silent production failures | Set up basic monitoring before accepting |
| "Only one person knows how X works" and that person is leaving | Critical knowledge loss | Make learning X the top priority |
| Certificate expires within 60 days with no renewal owner | Production outage risk | Assign renewal owner before accepting |

---

*Last updated: 2026-05-14 | Status: Template — fill in during KT sessions*
