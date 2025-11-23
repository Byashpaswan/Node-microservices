🚀 Node.js Microservices Architecture

This project is a Node.js-based Microservices System consisting of multiple independent services, each responsible for a specific domain. All external requests are routed through an API Gateway which forwards them to the appropriate microservice.




🧩 System Components
Service	Responsibility	Tech
API Gateway	Single entry point → routes request to services	Express.js, Reverse Proxy,rate-limit 
Identity Service	Authentication, Authorization, User Management	JWT, bcrypt, Database
Post Service	Create & manage posts	Express, Database
Media Service	Media upload & storage (images/videos)	File Storage / Cloud
Search Service	Search posts, users, media content	 / Query DB
RabbitMQ (Future integration)	Async communication between services	Message Broker



               ┌────────────────┐
               │  Client (UI)   │
               └───────┬────────┘
                       │ HTTP
                       ▼
                ┌───────────────┐
                │  API Gateway  │
                └──────┬────────┘
       ┌───────────────┼────────────────────┬───────────────┐
       ▼               ▼                    ▼               ▼
┌─────────────┐ ┌─────────────┐     ┌─────────────┐ ┌────────────────┐
│Identity     │ │ Post        │     │ Media       │ │ Search         │
│Service      │ │Service      │     │Service      │ │Service         │
└─────────────┘ └─────────────┘     └─────────────┘ └────────────────┘





⚙️ Tech Stack

   Node.js + Express.js 
   express-http-proxy, Redis ,express-rate-limit, helmet, winston logger

  Microservice Architecture

  JWT Authentication

  Docker + Docker Compose

 REST API

 RabbitMQ (Messaging - optional)