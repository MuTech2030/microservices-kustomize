# microservices-kustomize
This is to demo { Kustomize - Helm - ArgoCD &amp; Github Action CD } for Microservices based Solution to be deployed in Kubernetes 
Project Brief:
Quik is an end-to-end Generative AI platform for users to interact with top LLM models in ways that were never possible before.

By aggregating the AI experiences into a single, unified platform, Quik reduces cost, removes complexity, and unlocks advanced features like answer comparisons, productivity toolkits, smart collaboration, research optimization, and long-term memory retrievals with Graph RAG capabilities—features previously scattered across multiple apps.

DevOps Brief:
- Minimum deployment in the next 5 days.
- Scale to 200K users within the next 6 months.
- Backend is composed of two main services:
REST API service (contains all business logic) + Chat service (extracted independently for scalability)

Tech Stack:
Backend: Monolithic (not microservices)
Go(gin framework & ent ORM)
Postgresql DB
RestAPI
SMTP server
File storage EG S3

Frontend: Web apps (desktop and mobile)
React (TanStack)
Typescript

DevOps: Suggested Stack:
Kubernetes, Docker, Terraform, Helm/ArgoCD, GitOps, CI/CD
Cloud Infrastructure: AWS

** What we look for is the architecture that will allow a successful transition from an MVP to a scalable production-grade infrastructure, handling millions of users in the most cost-efficient approach.