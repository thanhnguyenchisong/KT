# Angular Frontend KT Checklist

Use this as a handover checklist so you do not miss important items.

## 1) Project Context
- [ ] Business goal and key user flows are documented.
- [ ] Scope boundaries are clear (what frontend owns vs backend/QA/DevOps owns).
- [ ] Main stakeholders and contacts are listed.
- [ ] Priority modules/pages are identified.

## 2) Local Setup
- [ ] Node, npm/pnpm, Angular CLI versions are documented.
- [ ] Setup steps from clone to run are tested on a clean machine.
- [ ] `.env` / config strategy is explained (without exposing secrets).
- [ ] Common setup issues and fixes are listed.

## 3) Architecture Walkthrough
- [ ] Folder structure is explained (`core`, `shared`, `features`, etc.).
- [ ] Routing strategy (lazy loading, guards, resolvers) is explained.
- [ ] State management approach is documented (RxJS/NgRx/signals).
- [ ] API layer pattern (services/interceptors/error handling) is clear.
- [ ] Reusable components/directives/pipes are introduced.

## 4) Angular Code Quality
- [ ] Smart vs presentational component pattern is followed.
- [ ] Change detection strategy is intentional (`OnPush` where needed).
- [ ] Subscription cleanup pattern is consistent (`takeUntil`, async pipe).
- [ ] Form strategy is consistent (Reactive Forms + validation messages).
- [ ] Strong typing is used for models and API responses.
- [ ] Linting and formatting pass (`eslint`, `prettier` if used).

## 5) UI/UX and Accessibility
- [ ] Responsive behavior is verified on key breakpoints.
- [ ] Loading, empty, error, and retry states are implemented.
- [ ] Accessibility basics are covered (labels, keyboard, focus, contrast).
- [ ] i18n/localization and date/number formats are validated.
- [ ] Design system/theme usage is consistent.

## 6) Testing
- [ ] Critical services/components have unit tests.
- [ ] Important user journeys have e2e tests (if framework exists).
- [ ] Mocking strategy for APIs is documented.
- [ ] Test commands and expected coverage are documented.

## 7) Performance and Security
- [ ] Bundle size checked and large dependencies reviewed.
- [ ] Lazy loading and code splitting are applied where needed.
- [ ] Caching/debounce/throttle applied to expensive flows.
- [ ] XSS-safe rendering and sanitization practices are followed.
- [ ] Auth token handling and interceptor behavior are verified.

## 8) Build, Release, and Environment
- [ ] Build configurations (`dev`, `staging`, `prod`) are documented.
- [ ] CI/CD pipeline steps are explained (build/test/deploy).
- [ ] Versioning/tagging/release note process is clear.
- [ ] Rollback strategy is documented.

## 9) KT Session Deliverables
- [ ] KT deck/doc includes architecture + key flows + troubleshooting.
- [ ] Live demo covers critical pages and edge cases.
- [ ] Session recording and notes are shared.
- [ ] FAQ and known issues list are included.
- [ ] Ownership handoff list (who maintains what) is finalized.

## 10) Post-KT Validation
- [ ] Receiver can run project independently.
- [ ] Receiver can fix one bug and ship one small change.
- [ ] Open risks and tech debt are logged with priority.
- [ ] Final sign-off from tech lead/manager is done.
