# Raman Hrynevich

**Backend-focused Full-Stack .NET Engineer** · C#, ASP.NET Core, React, Azure

I build backend-heavy web platforms where money, orders and access rights have to stay correct under load.
4+ years across FinTech, eCommerce and PropTech — from database design and API contracts to ADRs, CI/CD and production support.

[LinkedIn](https://www.linkedin.com/in/raman-hrynevich-080049414/) · [Telegram](https://t.me/ramanhrynevich) · [raman.hrynevich.dev@gmail.com](mailto:raman.hrynevich.dev@gmail.com)

<!-- Update the LinkedIn link after you set a custom URL (linkedin.com/in/raman-hrynevich). -->

---

### What I work on

- **Event-driven backends** — RabbitMQ, MassTransit, Azure Service Bus, Transactional Outbox, idempotent consumers
- **APIs that stay fast** — ASP.NET Core, EF Core, SQL Server / Azure SQL tuning with execution plans
- **Identity & security** — OAuth 2.0 / OpenID Connect, Auth0, Microsoft Entra ID, Keycloak, RBAC
- **Delivery** — Docker, Terraform, Azure DevOps, GitHub Actions, SonarQube quality gates
- **Frontend when the feature needs it** — React, TypeScript, Redux

### Selected results from production work

| Problem | What I did | Result |
| --- | --- | --- |
| Slow catalog and checkout APIs | EF Core projections, `AsNoTracking`, keyset pagination | p95 ~800 ms → ~250 ms |
| Credit decisions took days | Async scoring on Azure Service Bus inside the loan-origination workflow | ~2 days → under 4 hours |
| Slow repayment reports | Fixed missing indexes and N+1 queries found in execution plans | 10× faster |
| Paper visitor logs | Self-service kiosk check-in (React + ASP.NET Core) | ~3 min → under 1 min |

Commercial code is under NDA — the repositories below show the same engineering in the open.

### Projects

| Project | What it shows | Stack |
| --- | --- | --- |
| [**InMarket**](https://github.com/raman-hrynevich/InMarket) | Multi-vendor marketplace: services talking over RabbitMQ/MassTransit, Auth0 and Keycloak side by side, real-time notifications with SignalR | .NET, EF Core, SQL Server, MongoDB, Hangfire, React 19, TypeScript |
| **LedgerFlow** *(in progress)* | Payments and double-entry ledger: idempotent APIs, Transactional Outbox, concurrency-safe balances, load-tested | .NET 10, EF Core, MassTransit, Aspire, Testcontainers |
| **DocFlow AI** *(planned)* | Document intake with AI extraction, human review and an approval workflow — live on Azure | .NET 10, Azure Container Apps, Service Bus, Terraform, React |
| [**JIT vs AOT**](https://github.com/raman-hrynevich/JITvsAOTPresentation) | Talk: JIT vs Native AOT compilation in .NET | reveal.js |

<!-- Replace "(in progress)" / "(planned)" with links as soon as the repositories exist. -->

### Tech stack

- **Backend:** C#, .NET 8+, ASP.NET Core, EF Core, MediatR, FluentValidation, Serilog
- **Data:** SQL Server, Azure SQL, MongoDB
- **Messaging:** RabbitMQ, MassTransit, Azure Service Bus
- **Cloud & DevOps:** Azure (App Service, Functions, Service Bus, Key Vault, Application Insights), Docker, Terraform, Azure DevOps, GitHub Actions
- **Testing & quality:** xUnit, Moq, FluentAssertions, Jest, SonarQube / SonarCloud
- **Frontend:** React, TypeScript, Redux

### Currently

- Upgrading InMarket to .NET 10 and adding integration tests with Testcontainers
- Building LedgerFlow

<!-- Keep this section true: update it whenever your focus changes. -->
