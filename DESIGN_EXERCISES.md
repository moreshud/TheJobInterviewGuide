# System Design Exercises

- Define Actors/Stakeholders:
  - Customers: anyone interested in purchasing their products.
  - Merchants/Providers
  - Third party systems (sources of truth).
- Define limitations and trade-offs:
  - Design decisions (weaknesses & strengths).
  - Number of write/read Transactions per day/month.
- Create a high level system design:
  - Constraints and Assumptions.
  - Limitations & Unknowns.
  - Out of scope.
  - Define Non-functional and functional requirements.
  - Define Risks and Strategies (Bottlenecks, Restrictions, delimit edges, Troubleshooting scenarios)
  - Define Deployment Strategy: Treat configuration as code (Ansible, Terraform, Jenkins, Docker and Kubernetes) and Deploy services independently.
  - Scaling to enforce high cohesion and loose coupling (Redundancy / Consistency).
  - Availability patterns: **Fail-over** (load balancer, managing traffic and DNS using public IPs or CNAME records), **Database Replication** (Master-slave, master-master), Federation, Sharding, etc
  - Consider the **type of data**: Put transactional data into SQL, put JSON documents into a document database, put telemetry data into a time series data base, put application logs in Elasticsearch and put blobs in Azure Blob Storage.
  - Performance: use asynchronous messaging with a pub/sub architecture (Kibana) and backend services using RPC-style messaging protocol.
  - Monitoring: use distributed tracing (NewRelic, Splunk) to identify the cause of the failure (Traces should include a correlation ID).

## System Design Exercise - Amazon Dashboard

- Define Objective/Requeriments
  * Create a Search textbox for products
- Define Limitations
  * Ranking system
  * Number of products (database)
  * Number of categories (database)
  * Number of write Transactions per month
  * Number or read Transactions per month
- Out of Scope
  * Suggestions
  * Infinite scrolling
- Actions/Actors
  * Users (JWT roles)

## System Design Exercise - WhatsApp Messaging

### Round 1 - Core Design

Design WhatsApp-Scale Messaging — Core Design

Design the backend for a WhatsApp-like messaging system.

Data model: how do you store messages, conversations, users?
Delivery: how does message delivery work end-to-end (sender → server → recipient)?
Offline: how do you handle online vs offline recipients?

### Round 2 - Scale It

Design WhatsApp-Scale Messaging — Scale It

You now have 1B users, 100B messages/day (~1.15M msg/sec peak).

Bottlenecks: where does your Round 1 design break first?
Fan-out: how do you handle group chats with 1,000 members?

### Round 3 - Hard Problems

Design WhatsApp-Scale Messaging — Hard Problems

Pick one to go deep on:

- Exactly-once delivery guarantees
- Message ordering across devices (multi-device sync)
- End-to-end encryption key distribution at scale

## System Design Exercise - Facebook Fake Accounts

- Design a system that allow people to report fake accounts on Facebook

## Remember
- Are there any details I need?
- Are there any restrictions?
- What are all the major parts?
- Then, refine as much as possible.

## Credits:
- [The System Design Primer](https://github.com/donnemartin/system-design-primer)
- [Ten design principles for Azure applications](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles)
- [Evaluating Software Architectures for Real-Time Systems](https://www.researchgate.net/publication/220300661_Evaluating_Software_Architectures_for_Real-Time_Systems)
- [Architect's Guide to Frontend Frameworks](https://youtu.be/HI2vFGxiwkM)
- [BrowserDiet](https://browserdiet.com) - How to lose weight in the browser
- [System design: Como empezar el diseño de un sistema](https://youtu.be/kZNr1RfHhow)
- [AWS Whitepapers & Guides](https://aws.amazon.com/whitepapers/) - AWS technical content authored by AWS and the AWS community (technical guides and reference architecture diagrams).
- [Browse Azure Architectures](https://docs.microsoft.com/en-us/azure/architecture/browse/) - Architecture diagrams and technology descriptions for reference architectures, real world examples of cloud architectures.
- [Azure Cloud Design Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/) - useful design patterns for building reliable, scalable, secure applications in the cloud.
