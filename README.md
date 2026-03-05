# Software-Construction-Research-Assignment-
# Name: Wangolo Bachawa
# Reg no: M23B23/042
# Course: BSCS
# Year: 3:2

# 1. How Netflix Uses Microservices and How It Works for Them

Netflix pioneered the adoption of microservices architecture after experiencing a major outage in 2008 due to its monolithic system, which led to data corruption and downtime. The company migrated its entire infrastructure to Amazon Web Services (AWS) and restructured its application into over 1,000 independent microservices. These microservices handle specific functions such as user authentication, content recommendation, video encoding, streaming, and billing, communicating via well-defined APIs. This allows for polyglot development (using different programming languages for different services) and decentralized data management, where each microservice manages its own database to avoid dependencies and enable independent scaling.

The architecture emphasizes failure isolation through techniques like circuit breakers and bulkheads, preventing cascading failures. For instance, Netflix rebuilt its video processing pipeline using a microservices-based platform called Cosmos, which supports workflow-driven services for media encoding and processing billions of daily requests. This setup enables horizontal scaling, where services can be partitioned by workload, and real-time monitoring to quickly identify and resolve issues.

For Netflix, this approach has been highly successful: it supports over 250 million subscribers worldwide, handles millions of requests per second without interruptions, and allows rapid innovation. Benefits include improved resilience (one service failure doesn't affect others), faster deployment (teams own end-to-end service lifecycles), cost efficiency through optimized resource use, and seamless global scalability. However, it requires strong decoupling and robust API management to avoid complexity.

# 2. Other Companies That Use Microservices and How It Is Working for Them

Several major companies have adopted microservices for enhanced scalability, agility, and reliability. Below are key examples:

Amazon: Amazon transitioned from a monolithic architecture in the early 2000s to microservices hosted on AWS. This allows independent scaling of services like user authentication, product recommendations, and payments. It has worked exceptionally well, enabling Amazon to handle billions of daily transactions, reduce single points of failure, and support rapid feature deployment. Benefits include operational efficiency, faster market response, and a benchmark for eCommerce scalability, contributing to serving nearly 200 million monthly customers.

Uber: Uber switched from a monolith to microservices in response to global growth, dividing functions like driver management, passenger handling, billing, and notifications into independent services. This has improved performance by allowing parallel development and reduced operational pain points. It works effectively for Uber, supporting millions of rides daily with lower latency, better scalability, and easier debugging, leading to smoother business operations and innovation.

Spotify: Spotify employs microservices to manage its streaming platform for over 365 million users, with services handling playlists, recommendations, and user data independently. This architecture fosters continuous innovation and reliability. It has proven successful by enabling quick updates, reducing errors through decoupled teams, and providing a seamless user experience, which has driven user growth and high-quality service delivery.

eBay: eBay adopted microservices to handle 75 billion daily database calls, splitting its monolithic Ruby on Rails system into services for auctions, payments, and search. This has worked well by boosting stability, time-to-market, and scalability, allowing eBay to manage massive traffic without overloads and reducing duplicate engineering efforts across devices.

These companies report common benefits like faster development cycles, improved fault tolerance, and cost savings, though success depends on effective API management and team organization.

# 3. Companies That Were Using Microservices but Later Turned Back to Monolithic Architecture

While microservices offer advantages, some companies have reverted to monolithic or hybrid architectures due to complexity, high costs, and management challenges. Here are notable examples:

Amazon Prime Video: Prime Video initially used microservices for its Video Quality Analysis (VQA) system to monitor streaming quality. However, this led to high operational costs, complexity, and latency issues. In 2023, the team consolidated it into a monolithic architecture, reducing infrastructure costs by 90%, simplifying management, and improving performance. This shift was specific to a subsystem where microservices added unnecessary overhead, but it highlighted that monoliths can be more efficient for certain use cases.

Segment (now part of Twilio): Segment adopted microservices but found them difficult to manage at scale, leading to increased complexity and operational burdens. They consolidated services back into a monolithic or modular monolith for better efficiency and reduced maintenance overhead.

Uber: Uber, while largely microservices-based, consolidated parts of its marketplace and driver systems into monolith hybrids to simplify scaling and reduce cross-service latency where strict boundaries provided no added value.

Netflix: Netflix moved some internal workflows from pure microservices to monolith hybrids, recognizing that not all processes benefit from full decoupling.

These reversions often stem from microservices' drawbacks like distributed system complexity, higher debugging efforts, and costs, prompting companies to opt for monoliths in scenarios where simplicity outweighs modularity.
