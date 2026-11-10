# Workflow: New WebApp

## 1. Discover the brief
Identify product purpose, target users, primary journeys, constraints, integrations, budget/hosting constraints and success criteria. Ask only for information that materially changes the architecture or business behavior.

## 2. Define the product
Create `docs/PRD.md` for a substantial project. Include roles, user stories, business rules, edge cases, non-goals and acceptance criteria.

## 3. Select architecture
Compare viable stacks only when useful. Record frontend, backend, database, auth, storage, hosting, deployment and operational trade-offs in `docs/ARCHITECTURE.md`.

## 4. Define experience
Create `docs/DESIGN.md`: visual concept, tokens, page map, content hierarchy, responsive behavior, component rules, interaction states and accessibility expectations.

## 5. Scaffold
Initialize the project using verified commands for the chosen framework and current package ecosystem. Commit the lockfile. Set up environment examples with placeholders, not real secrets.

## 6. Build the critical path
Implement one end-to-end user journey at a time. Keep UI, domain logic, API and persistence connected. No fake buttons or placeholder-only core features.

## 7. Secure and test
Implement server-side authorization, validation and safe data access. Add tests for business rules, permissions and main browser journeys.

## 8. Review and ship
Apply the release gate. Deploy preview first where possible. Document setup, migrations, environment variables and limitations.
