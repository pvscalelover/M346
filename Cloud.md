# Cloud Computing Overview

## Virtualization Fundamentals

Virtualization is a foundational technology in cloud computing that creates a simulated, or 'virtual', computing environment as opposed to a physical one. This is facilitated by a hypervisor, a software that allows multiple operating systems to run on a single physical hardware host.

There are two main types of hypervisors:

- Type 1 (Bare-metal): This type runs directly on the host's hardware to control it and manage guest operating systems.
- Type 2 (Hosted): This type runs within a conventional operating system and supports guest operating systems.

The hypervisor enables the host machine to operate multiple virtual machines efficiently, utilizing resources such as memory and CPU cycles.

## Hyperscale Computing

Hyperscalers are the giants of cloud service providers, offering vast amounts of services like storage and computing at scale. The term "hyperscale" refers to the ability of an architecture to scale exponentially and quickly to respond to demand. Hyperscalers typically use Type 1 hypervisors for performance reasons.

Examples would be GCP, Azure, AWS.

Hetzner, Netcup etc. on the other hand, are "smaller" providers that typically aren't able to scale fast. In todays age they also mostly use Tier 1 hypervisors.
## Cloud Deployment Models

There are various cloud deployment models, each with its unique characteristics:

- On-Premise: Computing resources are fully contained within an enterprise's data center.
- Hybrid Cloud: A computing environment that uses on-premise infrastructure with cloud services.
- Cloud-Native: All applications and services are designed specifically for cloud deployment and used as such.

## Cloud Service Models

Cloud services are categorized based on the stack offered:

- Infrastructure as a Service (IaaS): This model provides virtualized physical computing resources.
- Platform as a Service (PaaS): Offers hardware and software tools hosted on the cloud.
- Software as a Service (SaaS): Software applications are hosted by service providers and made available to customers over the internet (You're making yourself dependant with this one.).
- Function as a Service (FaaS) or Serverless: Abstracts server management and focuses on the execution of code snippets. Example: Cloudflare Workers.

## Strategies for Cloud Migration

Organizations can adopt various methods for migrating applications to the cloud:

- Rehosting: Also a "Lift & Shift," involves moving applications to the cloud without changes.
- Replatforming: Involves making minimal adjustments to the application to take advantage of cloud capabilities.
- Refactoring/Replacing: Entails rewriting applications to be cloud-native and use cloud technologies such as load balancing more efficiently.
- Repurchasing: Involves moving to a different product, typically a SaaS solution. (In my opinion the worst. Own your software.)

## Cloud Storage Concepts

Cloud storage is categorized by access frequency:

- Hot Storage: For data that needs to be accessed frequently with minimal latency.
- Warm Storage: For data that is accessed less frequently but still needs to be readily available.
- Cold Storage: For data that is rarely accessed and stored for the long term.
- Databases: For structured data storage and retrieval. (Often low-latency)

## Cloud Networking

A cloud network's architecture is designed to deliver secure and scalable connectivity among resources. Key components include:

- Virtual Private Cloud (VPC): A secure, isolated private cloud hosted within a public cloud.
- Subnet: A segmented portion of a VPC designed to provide logical partitioning of services.
- Gateway: Manages the traffic between the internet and the private networks within the cloud.

These elements are essential for managing complex network architectures within the cloud.

## Scaling and Load Balancing

To accommodate changing loads, cloud resources can be scaled:

- Vertically (Scale Up): Adding more power to an existing machine.
- Horizontally (Scale Out): Adding more machines to a system.

Load balancers distribute traffic across multiple instances, and auto-scaling ensures resources are matched to the demand. I personally hate load balancers, as they tend to make the application you're designing overcomplicated. I just give the webapp (example) more resources.
