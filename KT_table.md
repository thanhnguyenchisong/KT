# Knowledge Transfer Handover Acceptance Checklist — Tracking Table

> **Usage**: Mark **Status** as `TODO`, `IN PROGRESS`, `DONE`, or `N/A`. Add notes in the **Remarks** column.

---

## 0.1 Source Code Transfer

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 1.01 | All source code repositories listed by name and URL | TODO | | |
| 1.02 | Frontend repository received and cloned | TODO | | |
| 1.03 | Backend repository received and cloned | TODO | | |
| 1.04 | Shared library/common module repositories received | TODO | | |
| 1.05 | Infrastructure-as-code repository received, if any | TODO | | |
| 1.06 | Deployment scripts repository received, if any | TODO | | |
| 1.07 | Documentation repository or wiki access received | TODO | | |
| 1.08 | Correct production branch identified | TODO | | |
| 1.09 | Latest production tag/commit SHA identified | TODO | | |
| 1.10 | **Production artifact verified to match a known repo commit** (deployed image tag/JAR matches source) | TODO | | |
| 1.11 | Current development branch identified | TODO | | |
| 1.12 | In-flight work identified: open PRs, unreleased hotfixes, half-merged feature branches | TODO | | |
| 1.13 | Repository access tested by cloning locally | TODO | | |
| 1.14 | Permission to create branch confirmed and tested | TODO | | |
| 1.15 | Permission to push branch confirmed and tested | TODO | | |
| 1.16 | Permission to create PR/MR confirmed and tested | TODO | | |
| 1.17 | Repo admin/maintainer ownership transferred, if required | TODO | | |
| 1.18 | Git LFS configured, if the repo uses large binary assets | TODO | | |
| 1.19 | Private npm registry access received and tested, if applicable | TODO | | |
| 1.20 | Private Maven/Gradle repository (Nexus, Artifactory) access received and tested, if applicable | TODO | | |

## 0.2 Application Access

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 2.01 | Local environment setup instructions received | TODO | | |
| 2.02 | Dev environment URL received and login tested | TODO | | |
| 2.03 | QA/UAT/staging environment URL received and login tested | TODO | | |
| 2.04 | Pre-production environment URL received and login tested, if any | TODO | | |
| 2.05 | Production environment URL received | TODO | | |
| 2.06 | Test user accounts received with credentials | TODO | | |
| 2.07 | Admin user account received, if applicable | TODO | | |
| 2.08 | Role/permission matrix received (which role can do what) | TODO | | |
| 2.09 | VPN access received and connection tested | TODO | | |
| 2.10 | SSO access received and login tested | TODO | | |
| 2.11 | Firewall/IP allowlist access confirmed, if required | TODO | | |
| 2.12 | Cloud IAM roles/permissions granted (specific policies, not just console access) | TODO | | |
| 2.13 | Email service (SendGrid, SES, etc.) account received | TODO | | |
| 2.14 | SMS/notification service account received | TODO | | |
| 2.15 | Payment gateway account received, if applicable | TODO | | |
| 2.16 | External API accounts with credentials received | TODO | | |
| 2.17 | Any other SaaS/vendor portals received | TODO | | |

## 0.3 Build And Run Verification

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 3.01 | Required Java version confirmed (exact version, e.g., JDK 17.0.x) | TODO | | |
| 3.02 | Required Node.js version confirmed (exact version, e.g., 18.x) | TODO | | |
| 3.03 | Required Angular version confirmed (exact version, e.g., 16.x) | TODO | | |
| 3.04 | Required Maven/Gradle version confirmed | TODO | | |
| 3.05 | Required npm/yarn/pnpm version confirmed | TODO | | |
| 3.06 | Docker and Docker Compose installed and working | TODO | | |
| 3.07 | `docker-compose.yml` or equivalent received and reviewed | TODO | | |
| 3.08 | Database container or local instance running | TODO | | |
| 3.09 | Redis/cache container running, if required | TODO | | |
| 3.10 | Kafka/RabbitMQ/message broker container running, if required | TODO | | |
| 3.11 | Elasticsearch/search engine container running, if required | TODO | | |
| 3.12 | Any other local service dependencies running | TODO | | |
| 3.13 | Backend builds successfully on local machine | TODO | | |
| 3.14 | Frontend builds successfully on local machine | TODO | | |
| 3.15 | Backend runs locally | TODO | | |
| 3.16 | Frontend runs locally | TODO | | |
| 3.17 | Frontend can call backend locally (proxy/CORS working) | TODO | | |
| 3.18 | Unit tests can run locally and pass | TODO | | |
| 3.19 | Integration tests can run locally, if available | TODO | | |
| 3.20 | E2E tests can run locally, if available | TODO | | |
| 3.21 | Required environment variables documented with example values | TODO | | |
| 3.22 | Required config files/templates received (`.env.example`, `application-local.yml`, etc.) | TODO | | |
| 3.23 | Required local certificates received, if any | TODO | | |
| 3.24 | "Clean machine to running app" guide written and verified | TODO | | |

## 0.4 Database And Data

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 4.01 | Database engine and exact version confirmed (e.g., PostgreSQL 15.3) | TODO | | |
| 4.02 | Database schema received | TODO | | |
| 4.03 | Migration tool identified (Flyway, Liquibase) and migration files received | TODO | | |
| 4.04 | How to create and apply a new migration documented | TODO | | |
| 4.05 | Seed/reference data received | TODO | | |
| 4.06 | ERD or schema documentation received | TODO | | |
| 4.07 | Dev database access tested: can connect via CLI/IDE, run a SELECT, see expected tables | TODO | | |
| 4.08 | Staging/UAT database access tested: same verification as dev | TODO | | |
| 4.09 | Production database access policy clarified (read-only? bastion host? approval needed?) | TODO | | |
| 4.10 | Production data volume documented (approximate size in GB, row counts for large tables) | TODO | | |
| 4.11 | Stored procedures, triggers, views, and functions documented, if any | TODO | | |
| 4.12 | Database connection pool configuration documented (HikariCP settings, max connections) | TODO | | |
| 4.13 | High-write tables vs. read-heavy tables identified | TODO | | |
| 4.14 | Indexes documented with their purpose | TODO | | |
| 4.15 | Soft delete vs. hard delete approach documented | TODO | | |
| 4.16 | Known data integrity issues documented (orphaned records, constraint violations) | TODO | | |
| 4.17 | Database user accounts listed; old team credentials scheduled for rotation | TODO | | |
| 4.18 | Backup process documented with schedule and retention | TODO | | |
| 4.19 | Restore process documented and tested (or at minimum, walked through) | TODO | | |
| 4.20 | Data masking/anonymization process for non-prod environments documented | TODO | | |
| 4.21 | Sensitive/PII data locations documented | TODO | | |

## 0.5 Deployment And Operations

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 5.01 | CI/CD system access received and login tested | TODO | | |
| 5.02 | Pipeline configuration file location identified (Jenkinsfile, `.github/workflows/`, etc.) | TODO | | |
| 5.03 | Pipeline stages documented (build, test, lint, scan, package, deploy) | TODO | | |
| 5.04 | Build artifact registry access received and tested | TODO | | |
| 5.05 | Docker/container registry access received and tested, if applicable | TODO | | |
| 5.06 | Cloud console access received with specific IAM permissions verified | TODO | | |
| 5.07 | Kubernetes/hosting platform access received and tested (`kubectl get pods` works), if applicable | TODO | | |
| 5.08 | Deployment process documented as step-by-step runbook for each environment | TODO | | |
| 5.09 | Deployment order/dependencies documented (e.g., DB migration before backend, backend before frontend) | TODO | | |
| 5.10 | Environment-specific configuration differences documented (what differs between dev/staging/prod) | TODO | | |
| 5.11 | Deployment strategy documented (rolling update, blue/green, canary) | TODO | | |
| 5.12 | Developer has deployed to dev environment independently | TODO | | |
| 5.13 | Developer has deployed to staging/UAT environment independently | TODO | | |
| 5.14 | Production deployment approval process documented (who approves, what gates exist) | TODO | | |
| 5.15 | **Rollback procedure documented AND rehearsed on staging** | TODO | | |
| 5.16 | Health check endpoints documented with expected responses | TODO | | |
| 5.17 | Smoke test checklist received (automated or manual) | TODO | | |
| 5.18 | Scheduled maintenance windows documented | TODO | | |
| 5.19 | Upcoming planned events documented (customer go-lives, migrations, etc.) | TODO | | |

## 0.6 Monitoring And Support

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 6.01 | Application logs access received and verified (can search and find a specific request) | TODO | | |
| 6.02 | Production logs access policy clarified | TODO | | |
| 6.03 | Example log queries provided for common troubleshooting scenarios | TODO | | |
| 6.04 | Structured logging key fields documented (correlation ID, user ID, request ID) | TODO | | |
| 6.05 | Monitoring dashboard access received and key dashboards identified | TODO | | |
| 6.06 | SLA/SLO targets documented (response time P95, error rate threshold, uptime %) | TODO | | |
| 6.07 | Key metrics explained: what "healthy" looks like numerically | TODO | | |
| 6.08 | Alerting tool access received and alert rules reviewed | TODO | | |
| 6.09 | Error tracking tool access received, if any (Sentry, Bugsnag, etc.) | TODO | | |
| 6.10 | Top 10 common production issues documented with symptoms, root cause, and resolution steps | TODO | | |
| 6.11 | Incident escalation path received with names, roles, and contact methods | TODO | | |
| 6.12 | On-call process documented (rotation, response SLA per severity) | TODO | | |
| 6.13 | Support contact list received (business, infra, security, QA, vendor contacts) | TODO | | |
| 6.14 | Support ticket history reviewed (what do users actually complain about) | TODO | | |
| 6.15 | Last 6-12 months of incident history received with root causes and fixes | TODO | | |

## 0.7 Security And Secrets

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 7.01 | Secret manager access received and verified (can list, read, and if authorized, rotate) | TODO | | |
| 7.02 | Location of all secrets documented (which secrets, which manager, which environment) | TODO | | |
| 7.03 | Secret rotation process documented with schedule | TODO | | |
| 7.04 | API keys ownership clarified and transferred to incoming team accounts | TODO | | |
| 7.05 | OAuth/SSO client configuration documented | TODO | | |
| 7.06 | SSL/TLS certificate ownership clarified | TODO | | |
| 7.07 | **SSL/TLS certificate expiry dates documented with renewal owners assigned** | TODO | | |
| 7.08 | Domain/DNS ownership clarified | TODO | | |
| 7.09 | CORS configuration documented | TODO | | |
| 7.10 | Rate limiting configuration documented | TODO | | |
| 7.11 | WAF rules documented, if applicable | TODO | | |
| 7.12 | Security scan process documented (SAST, DAST, dependency scanning) | TODO | | |
| 7.13 | Penetration test results reviewed, if available | TODO | | |
| 7.14 | Known vulnerabilities reviewed with remediation status | TODO | | |
| 7.15 | No secrets are hardcoded in source code (verified by scan) | TODO | | |
| 7.16 | Compliance requirements documented (GDPR, HIPAA, PCI-DSS, etc.) | TODO | | |
| 7.17 | **Outgoing team access revocation plan with timeline** | TODO | | |

## 0.8 Business And Product Knowledge

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 8.01 | Business purpose of the application explained and incoming developer can explain it back | TODO | | |
| 8.02 | Main users and roles understood (incoming developer can list them) | TODO | | |
| 8.03 | SLA commitments to customers/stakeholders documented | TODO | | |
| 8.04 | Top 5 user journeys walked through end-to-end (UI to API to DB and back) | TODO | | |
| 8.05 | Top 3 complex business flows walked through with code | TODO | | |
| 8.06 | Current backlog reviewed | TODO | | |
| 8.07 | In-progress work reviewed and status documented | TODO | | |
| 8.08 | Known bugs reviewed with workarounds | TODO | | |
| 8.09 | Technical debt inventory reviewed with priority ranking | TODO | | |
| 8.10 | Upcoming roadmap reviewed for next 1-2 quarters | TODO | | |
| 8.11 | Business owner/contact identified with communication channel | TODO | | |
| 8.12 | Peak usage periods documented (time of day, end of month, seasonal) | TODO | | |

## 0.9 Ownership Transfer

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 9.01 | Code repository ownership transferred (admin rights) | TODO | | |
| 9.02 | CI/CD pipeline ownership transferred | TODO | | |
| 9.03 | Deployment ownership transferred | TODO | | |
| 9.04 | Monitoring and alerting ownership transferred | TODO | | |
| 9.05 | Incident response ownership transferred | TODO | | |
| 9.06 | Vendor/service account ownership transferred, if applicable | TODO | | |
| 9.07 | Domain/DNS ownership transferred, if applicable | TODO | | |
| 9.08 | Cloud/resource billing owner identified and documented | TODO | | |
| 9.09 | **Monthly infrastructure cost documented and budget alerts configured** | TODO | | |
| 9.10 | Auto-scaling configuration and resource limits documented | TODO | | |
| 9.11 | License/subscription renewal dates and owners documented | TODO | | |
| 9.12 | **Third-party service billing transferred to incoming team accounts** | TODO | | |
| 9.13 | Transition/shadow period agreed (2-4 weeks of parallel operation recommended) | TODO | | |
| 9.14 | Post-handover support agreement documented: duration, response SLA, escalation channel | TODO | | |
| 9.15 | Knowledge escrow plan: what happens if outgoing team becomes unreachable | TODO | | |
| 9.16 | Final KT sign-off date agreed | TODO | | |

## 0.10 Final Acceptance Criteria

### Mandatory (all must pass before sign-off)

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 10.01 | Production artifact verified to match a known repo commit | TODO | | |
| 10.02 | Developer set up the full project on a clean machine without assistance | TODO | | |
| 10.03 | Developer ran all test suites (unit, integration, E2E) and can interpret results | TODO | | |
| 10.04 | Developer made a code change and deployed it to dev/staging independently | TODO | | |
| 10.05 | Developer performed a rollback on staging successfully | TODO | | |
| 10.06 | Developer investigated a real past production issue from logs to root cause without help | TODO | | |
| 10.07 | Developer can draw the system architecture from memory and explain data flow | TODO | | |
| 10.08 | Developer can list all external integrations, their owners, and fallback behavior | TODO | | |
| 10.09 | All secrets are accessible to incoming team and not hardcoded | TODO | | |
| 10.10 | Outgoing team access revocation schedule is documented and agreed | TODO | | |
| 10.11 | Post-handover support window is documented: duration, SLA, escalation channel | TODO | | |
| 10.12 | Third-party service accounts transferred or billing ownership clarified | TODO | | |
| 10.13 | Certificate and license expiry calendar created with renewal owners assigned | TODO | | |
| 10.14 | Both teams sign the handover acceptance document with date | TODO | | |

### Recommended (complete within 2 weeks post-handover)

| # | Checklist Item | Status | Owner | Remarks |
|---|---|---|---|---|
| 10.15 | Developer handled a real production alert or incident (shadowed or solo) | TODO | | |
| 10.16 | Developer performed a production deployment following the full release process | TODO | | |
| 10.17 | Developer onboarded another team member using the documentation created during KT | TODO | | |
| 10.18 | Developer wrote or updated at least one runbook based on real operational experience | TODO | | |

---

*Last updated: 2026-05-14 | Status: Template — fill in during KT sessions*
