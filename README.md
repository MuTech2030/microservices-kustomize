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
-------------
after I do one e2e process successfully -> Ai Module Consistency -> 
-------------
For now I just want you to understand my stratigy for working with you in creating things I want, 
now I want you to : 
    1. read my repo of helm charts for deploying my rhesis microservices that will contain 5 microservices based solution (now I just created one, I want you to create the other 4 in the same style), then lint each helm you created, (use dummy images name for now )
    2. use trivy to scan each chart -> then fix each chart vulnerabilities
    3. Correct naming conventions.
    4. add the docs like read me and other needed docs to make it look professional and prod grade.
    5. show me all the steps you did to create the helm charts so I can do that by going online in future, be brief , but show the steps that would make anyone achive the same results when creating helm charts for an app
    6. read my repo of 2ed helm charts for enablers and create all the enablers I mention below (make sure they are enterprise prod grade & in the same style of my repo) :
        for Azure AKS:
            a. Nginx Ingress.
            b. LGTM , a chart for each component and microservices mode
            c. Defender daemonset for Azure Policy
            d. Defender deamonset for Cloud Workload Protection
            e. Calico for Network Policy
            f. DataDog Deamonset for metrics, traces, logs
            g. Azure Monitor Daemonset for logs & metrics & alerting
            h. ISTIO Ingress
            i. All csi drivers for storage, secrets KeyVault, ...
            j. azure external dns 
        for AWS EKS: 
            a. Nginx Ingress.
            b. LGTM , a chart for each component and microservices mode
            c.  AWS Audit Manager Policy
            d. Guarduty for Cloud Workload Protection
            e. Calico for Network Policy
            f. DataDog Deamonset for metrics, traces, logs
            g. AWS CloudWatch Daemonset for logs & metrics & alerting
            h. ISTIO Ingress
            i. All csi drivers for storage, aws secrets manager, ...
            j. external dns
    7. use trivy to scan each chart -> then fix each chart vulnerabilities
    8. Correct naming conventions.
    9. add the docs like read me and other needed docs to make it look professional and prod grade.
    10. show me all the steps you did to create the helm charts so I can do that by going online in future, be brief , but show the steps that would make anyone achive the same results when creating helm charts for an app

--------------
For now I just want you to understand my stratigy for working with you in creating things I want, 
now I want you to : 
    1. read my repo of kustomize charts for deploying my rhesis microservices that will contain 5 microservices based solution (now I just created one, I want you to create the other 4 in the same style), then lint each kustomize you created, (use dummy images name for now )
    2. use trivy to scan each chart -> then fix each chart vulnerabilities
    3. Correct naming conventions.
    4. add the docs like read me and other needed docs to make it look professional and prod grade.
    5. show me all the steps you did to create the kustomize charts so I can do that by going online in future, be brief , but show the steps that would make anyone achive the same results when creating kustomize charts for an app
    6. read my repo of 2ed kustomize charts for enablers and create all the enablers I mention below (make sure they are enterprise prod grade & in the same style of my repo) :
        for Azure AKS:
            a. Nginx Ingress.
            b. LGTM , a chart for each component and microservices mode
            c. Defender daemonset for Azure Policy
            d. Defender deamonset for Cloud Workload Protection
            e. Calico for Network Policy
            f. DataDog Deamonset for metrics, traces, logs
            g. Azure Monitor Daemonset for logs & metrics & alerting
            h. ISTIO Ingress
            i. All csi drivers for storage, secrets KeyVault, ...
            j. azure external dns 
        for AWS EKS: 
            a. Nginx Ingress.
            b. LGTM , a chart for each component and microservices mode
            c.  AWS Audit Manager Policy
            d. Guarduty for Cloud Workload Protection
            e. Calico for Network Policy
            f. DataDog Deamonset for metrics, traces, logs
            g. AWS CloudWatch Daemonset for logs & metrics & alerting
            h. ISTIO Ingress
            i. All csi drivers for storage, aws secrets manager, ...
            j. external dns
    7. use trivy to scan each chart -> then fix each chart vulnerabilities
    8. Correct naming conventions.
    9. add the docs like read me and other needed docs to make it look professional and prod grade.
    10. show me all the steps you did to create the kustomize charts so I can do that by going online in future, be brief , but show the steps that would make anyone achive the same results when creating kustomize charts for an app

--------------
For now I just want you to understand my stratigy for working with you in creating things I want, 
now I want you to : 
    1. read my repo of azure terraform modules for deploying azure solutions.
    2. I want you to create all the follwoing modules : 
        a. AKS
        b. Databases PaaS:
            . MySQL ,
            . Postgress,
            . SQL DBs,
        c. Azure Blob Storage
        d. Azure File Storage
        e. Azure Load Balancer
        e. Azure App Load Balancer
        f. Azure VM
        g. Azure VMSS
        # h. Azure App Service
        i. Azure KeyValut
        j. Azure Service Bus
        k. Azure RabbitMQ
        l. Azure Disks
        m. Azure Back up Vault
        n. Azure Back up Policy
        o. Azure DR Vault
        p. Azure Docker Registery
        q. Azure Image Registry
        s. Azure Workload Identity
        t. Azure Managed Identity
        u. Azure Vnets
        v. Azure Routing Tables
        w. Azure Secrutiy Groups
        x. Azure Peering
        y. Azure DNS , public zones & private zones
        z. Azure Defender Enablement
    3. by using my sonar Cloud account , scan every module & fix the security reports
    4. add docs to each module 

----------------
    # same for aws
    # also creating apps once I share the app design
    ....
    
