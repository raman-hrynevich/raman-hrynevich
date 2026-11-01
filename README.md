# Raman Hrynevich

**Backend-focused Full-Stack .NET Engineer** · C#, ASP.NET Core, React, Azure

I build backend-heavy web platforms where money, orders and access rights have to stay correct under load.
4+ years across FinTech, eCommerce and PropTech — from database design and API contracts to ADRs, CI/CD and production support.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230A66C2.svg?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyBmaWxsPSIjZmZmZmZmIiByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMjAuNDQ3IDIwLjQ1MmgtMy41NTR2LTUuNTY5YzAtMS4zMjgtLjAyNy0zLjAzNy0xLjg1Mi0zLjAzNy0xLjg1MyAwLTIuMTM2IDEuNDQ1LTIuMTM2IDIuOTM5djUuNjY3SDkuMzUxVjloMy40MTR2MS41NjFoLjA0NmMuNDc3LS45IDEuNjM3LTEuODUgMy4zNy0xLjg1IDMuNjAxIDAgNC4yNjcgMi4zNyA0LjI2NyA1LjQ1NXY2LjI4NnpNNS4zMzcgNy40MzNjLTEuMTQ0IDAtMi4wNjMtLjkyNi0yLjA2My0yLjA2NSAwLTEuMTM4LjkyLTIuMDYzIDIuMDYzLTIuMDYzIDEuMTQgMCAyLjA2NC45MjUgMi4wNjQgMi4wNjMgMCAxLjEzOS0uOTI1IDIuMDY1LTIuMDY0IDIuMDY1em0xLjc4MiAxMy4wMTlIMy41NTVWOWgzLjU2NHYxMS40NTJ6TTIyLjIyNSAwSDEuNzcxQy43OTIgMCAwIC43NzQgMCAxLjcyOXYyMC41NDJDMCAyMy4yMjcuNzkyIDI0IDEuNzcxIDI0aDIwLjQ1MUMyMy4yIDI0IDI0IDIzLjIyNyAyNCAyMi4yNzFWMS43MjlDMjQgLjc3NCAyMy4yIDAgMjIuMjIyIDBoLjAwM3oiLz48L3N2Zz4%3D)](https://www.linkedin.com/in/raman-hrynevich-080049414/) [![Telegram](https://img.shields.io/badge/Telegram-%232CA5E0.svg?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/ramanhrynevich) [![Gmail](https://img.shields.io/badge/Gmail-%23D14836.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:raman.hrynevich.dev@gmail.com)

<!-- Update the LinkedIn link after you set a custom URL (linkedin.com/in/raman-hrynevich). -->

---

### What I work on

- **Event-driven backends** — RabbitMQ, MassTransit, Azure Service Bus, Transactional Outbox, idempotent consumers
- **APIs that stay fast** — ASP.NET Core, EF Core, SQL Server / Azure SQL tuning with execution plans
- **Identity & security** — OAuth 2.0 / OpenID Connect, Auth0, Microsoft Entra ID, Keycloak, RBAC
- **Delivery** — Docker, Terraform, Azure DevOps, GitHub Actions, SonarQube quality gates
- **Frontend when the feature needs it** — React, TypeScript, Redux

### Selected results from production work

| Context | What I did | Result |
| --- | --- | --- |
| **Multi-vendor marketplace** (eCommerce) · catalog and checkout APIs slowed down on large product lists | Rewrote hot queries as EF Core projections with `AsNoTracking`, replaced offset paging with keyset pagination, added covering and filtered indexes on Azure SQL based on execution plans | p95 latency **~800 ms → ~250 ms** (~3× faster) |
| **Multi-vendor marketplace** · order events between services could be lost or handled twice | Event-driven order flow on RabbitMQ + MassTransit with EF Core Transactional Outbox and idempotent consumers | **No lost or duplicate** order events |
| **Multi-vendor marketplace** · storefront, seller portal and admin panel each had their own login | Moved all three apps to one identity provider: Auth0, OAuth 2.0 / OpenID Connect, role-based access | **3 separate logins → 1** single sign-on |
| **SME lending platform** (FinTech) · credit decisions waited on manual underwriter work | Built the loan-origination workflow end to end (application → verification → scoring → e-signature): async scoring on Azure Service Bus, banking and registry APIs, DocuSign webhooks with idempotent handling | Credit decision time **~2 days → under 4 hours** |
| **SME lending platform** · repayment and penalty reports were slow | Found missing indexes and N+1 queries in EF Core through execution plans and fixed them | Report generation **10× faster** |
| **Smart office platform** (PropTech) · visitors signed paper logs at reception | Self-service kiosk check-in (React/Redux touch UI + ASP.NET Core API) with near-real-time host alerts over Azure Service Bus and RabbitMQ | Check-in **~3 min → under 1 min** per visitor |
| **Smart office platform** · releases required downtime | Azure DevOps CI/CD with App Service deployment slots | **Zero-downtime** releases |

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

![C#](https://img.shields.io/badge/C%23-%23239120.svg?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyBmaWxsPSIjZmZmZmZmIiByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMS4xOTQgNy41NDN2OC45MTNjMCAxLjEwMy41ODggMi4xMjIgMS41NDQgMi42NzRsNy43MTggNC40NTZhMy4wODYgMy4wODYgMCAwIDAgMy4wODggMGw3LjcxOC00LjQ1NmEzLjA4NyAzLjA4NyAwIDAgMCAxLjU0NC0yLjY3NFY3LjU0M2EzLjA4NCAzLjA4NCAwIDAgMC0xLjU0NC0yLjY3M0wxMy41NDQuNDE0YTMuMDg2IDMuMDg2IDAgMCAwLTMuMDg4IDBMMi43MzggNC44N2EzLjA4NSAzLjA4NSAwIDAgMC0xLjU0NCAyLjY3M1ptNS40MDMgMi45MTR2My4wODdhLjc3Ljc3IDAgMCAwIC43NzIuNzcyLjc3My43NzMgMCAwIDAgLjc3Mi0uNzcyLjc3My43NzMgMCAwIDEgMS4zMTctLjU0Ni43NzUuNzc1IDAgMCAxIC4yMjYuNTQ2IDIuMzE0IDIuMzE0IDAgMSAxLTQuNjMxIDB2LTMuMDg3YzAtLjYxNS4yNDQtMS4yMDMuNjc5LTEuNjM3YTIuMzEyIDIuMzEyIDAgMCAxIDMuMjc0IDBjLjQzNC40MzQuNjc4IDEuMDIzLjY3OCAxLjYzN2EuNzY5Ljc2OSAwIDAgMS0uMjI2LjU0NS43NjcuNzY3IDAgMCAxLTEuMDkxIDAgLjc3Ljc3IDAgMCAxLS4yMjYtLjU0NS43Ny43NyAwIDAgMC0uNzcyLS43NzIuNzcxLjc3MSAwIDAgMC0uNzcyLjc3MlptMTIuMzUgMy4wODdhLjc3Ljc3IDAgMCAxLS43NzIuNzcyaC0uNzcydi43NzJhLjc3My43NzMgMCAwIDEtMS41NDQgMHYtLjc3MmgtMS41NDR2Ljc3MmEuNzczLjc3MyAwIDAgMS0xLjMxNy41NDYuNzc1Ljc3NSAwIDAgMS0uMjI2LS41NDZ2LS43NzJIMTJhLjc3MS43NzEgMCAxIDEgMC0xLjU0NGguNzcydi0xLjU0M0gxMmEuNzcuNzcgMCAxIDEgMC0xLjU0NGguNzcydi0uNzcyYS43NzMuNzczIDAgMCAxIDEuMzE3LS41NDYuNzc1Ljc3NSAwIDAgMSAuMjI2LjU0NnYuNzcyaDEuNTQ0di0uNzcyYS43NzMuNzczIDAgMCAxIDEuNTQ0IDB2Ljc3MmguNzcyYS43NzIuNzcyIDAgMCAxIDAgMS41NDRoLS43NzJ2MS41NDNoLjc3MmEuNzc2Ljc3NiAwIDAgMSAuNzcyLjc3MlptLTMuMDg4LTIuMzE1aC0xLjU0NHYxLjU0M2gxLjU0NHYtMS41NDNaIi8%2BPC9zdmc%2B) ![.NET](https://img.shields.io/badge/.NET-%23512BD4.svg?style=for-the-badge&logo=.net&logoColor=white) ![SQL Server](https://img.shields.io/badge/SQL%20Server-%23CC2927.svg?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0iI2ZmZmZmZiI%2BPGVsbGlwc2UgY3g9IjEyIiBjeT0iNSIgcng9IjgiIHJ5PSIzIi8%2BPHBhdGggZD0iTTQgN3Y0YzAgMS42NiAzLjU4IDMgOCAzczgtMS4zNCA4LTNWN2MwIDEuNjYtMy41OCAzLTggM1M0IDguNjYgNCA3em0wIDZ2NGMwIDEuNjYgMy41OCAzIDggM3M4LTEuMzQgOC0zdi00YzAgMS42Ni0zLjU4IDMtOCAzcy04LTEuMzQtOC0zeiIvPjwvc3ZnPg%3D%3D) ![MongoDB](https://img.shields.io/badge/MongoDB-%2347A248.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![RabbitMQ](https://img.shields.io/badge/RabbitMQ-%23FF6600.svg?style=for-the-badge&logo=rabbitmq&logoColor=white)

![React](https://img.shields.io/badge/React-%2320232A.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-%233178C6.svg?style=for-the-badge&logo=typescript&logoColor=white) ![Redux](https://img.shields.io/badge/Redux-%23764ABC.svg?style=for-the-badge&logo=redux&logoColor=white)

![Azure](https://img.shields.io/badge/Azure-%230078D4.svg?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyBmaWxsPSIjZmZmZmZmIiByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMjIuMzc5IDIzLjM0M2ExLjYyIDEuNjIgMCAwIDAgMS41MzYtMi4xNHYuMDAyTDE3LjM1IDEuNzZBMS42MiAxLjYyIDAgMCAwIDE1LjgxNi42NTdIOC4xODRBMS42MiAxLjYyIDAgMCAwIDYuNjUgMS43NkwuMDg2IDIxLjIwNGExLjYyIDEuNjIgMCAwIDAgMS41MzYgMi4xMzloNC43NDFhMS42MiAxLjYyIDAgMCAwIDEuNTM1LTEuMTAzbC45NzctMi44OTIgNC45NDcgMy42NzVjLjI4LjIwOC42MTguMzIuOTY2LjMybS0zLjA4NC0xMi41MzEgMy42MjQgMTAuNzM5YS41NC41NCAwIDAgMS0uNTEuNzEzdi0uMDAxaC0uMDNhLjU0LjU0IDAgMCAxLS4zMjItLjEwNmwtOS4yODctNi45aDQuODUzbTYuMzEzIDcuMDA2Yy4xMTYtLjMyNi4xMy0uNjk0LjAwNy0xLjA1OEw5Ljc5IDEuNzZhMS43MjIgMS43MjIgMCAwIDAtLjAwNy0uMDJoNi4wMzRhLjU0LjU0IDAgMCAxIC41MTIuMzY2bDYuNTYyIDE5LjQ0NWEuNTQuNTQgMCAwIDEtLjMzOC42ODQiLz48L3N2Zz4%3D) ![Azure DevOps](https://img.shields.io/badge/Azure%20DevOps-%230078D7.svg?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyBmaWxsPSIjZmZmZmZmIiByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMCA4Ljg3N0wyLjI0NyA1LjkxbDguNDA1LTMuNDE2Vi4wMjJsNy4zNyA1LjM5M0wyLjk2NiA4LjMzOHY4LjIyNUwwIDE1LjcwN3ptMjQtNC40NXYxNC42NTFsLTUuNzUzIDQuOS05LjMwMy0zLjA1N3YzLjA1NmwtNS45NzgtNy40MTYgMTUuMDU3IDEuNzk4VjUuNDE1eiIvPjwvc3ZnPg%3D%3D) ![Docker](https://img.shields.io/badge/Docker-%232496ED.svg?style=for-the-badge&logo=docker&logoColor=white) ![Terraform](https://img.shields.io/badge/Terraform-%237B42BC.svg?style=for-the-badge&logo=terraform&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-%232088FF.svg?style=for-the-badge&logo=githubactions&logoColor=white)

![Auth0](https://img.shields.io/badge/Auth0-%23EB5424.svg?style=for-the-badge&logo=auth0&logoColor=white) ![Keycloak](https://img.shields.io/badge/Keycloak-%234D4D4D.svg?style=for-the-badge&logo=keycloak&logoColor=white) ![SonarQube](https://img.shields.io/badge/SonarQube-%23126ED3.svg?style=for-the-badge&logo=sonarqubecloud&logoColor=white)

### Currently

- Upgrading InMarket to .NET 10 and adding integration tests with Testcontainers
- Building LedgerFlow

<!-- Keep this section true: update it whenever your focus changes. -->
