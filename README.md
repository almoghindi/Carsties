# Carsties

Carsties is an advanced application developed using .NET and Next.js with a microservices architecture. This repository demonstrates how to build and deploy a microservices-based application.

## Features

- **Microservices Architecture:** Multiple backend services built with .NET.
- **Client Application:** Frontend built with Next.js.
- **Service Communication:** Utilizes RabbitMQ and gRPC.
- **Identity Management:** Integrated with Duende IdentityServer.
- **Gateway:** Uses Microsoft YARP as a gateway.
- **Real-Time Updates:** Employs SignalR for push notifications.
- **Containerization:** Dockerized services.
- **CI/CD:** GitHub Actions for continuous integration and delivery.
- **Deployment:** Local deployment with Docker Compose and Kubernetes, including publishing to an online Kubernetes cluster.
- **Testing:** Unit and integration testing using XUnit.

## Microservices Overview

### AuctionService
- **Functionality:** Manages auction-related operations.
- **Key Features:**
  - Creating and managing auction listings.
  - Handling auction start and end times.
  - Processing auction bids and determining winners.
  - Integrating with the BiddingService for bid management.

### BiddingService
- **Functionality:** Manages the bidding process within auctions.
- **Key Features:**
  - Recording bids from users.
  - Validating bid amounts and user eligibility.
  - Providing real-time bid updates using SignalR.
  - Ensuring that the highest bid is correctly reflected in the AuctionService.

### Contracts
- **Functionality:** Defines shared interfaces and models used across different microservices.
- **Key Features:**
  - Common data models for consistency.
  - Interfaces for service-to-service communication.
  - Shared utility functions and constants.

### GatewayService
- **Functionality:** Acts as the API gateway for the application, routing requests to appropriate microservices.
- **Key Features:**
  - Centralized entry point for client applications.
  - Request routing to backend microservices.
  - Authentication and authorization enforcement using IdentityService.
  - Load balancing and request validation.

### IdentityService
- **Functionality:** Manages user authentication and authorization.
- **Key Features:**
  - User registration and login.
  - Issuing and validating JWT tokens.
  - Integrating with Duende IdentityServer for OAuth2 and OpenID Connect.
  - Managing user roles and permissions.

### NotificationService
- **Functionality:** Manages notifications for the application.
- **Key Features:**
  - Sending real-time notifications using SignalR.
  - Handling email and SMS notifications.
  - Integrating with other services to notify users about important events (e.g., outbid notifications, auction wins).

### SearchService
- **Functionality:** Provides search capabilities for auction listings and bids.
- **Key Features:**
  - Indexing auction listings and bids using MongoDB.
  - Handling search queries from users.
  - Returning relevant search results quickly.
  - Supporting advanced search features like filters and sorting.

## Tools and Technologies

- **.NET**
- **ASP.NET**
- **Next.js**
- **RabbitMQ**
- **Duende IdentityServer**
- **Microsoft YARP**
- **SignalR**
- **Docker**
- **Kubernetes**
- **GitHub Actions**
- **XUnit** (for unit and integration testing)

## Databases

- **MongoDB**
- **PostgreSQL**

## Getting Started

### Prerequisites

- Coding experience
- Windows, Mac, or Linux computer capable of running Docker

### Installation

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/almoghindi/Carsties.git
    cd Carsties
    ```

2. **Install Docker Desktop:** Ensure Docker is installed and running on your machine. Follow the [Docker installation instructions](https://docs.docker.com/desktop/).

3. **Build the Services:**
    ```bash
    docker compose build
    ```

4. **Run the Services:**
    ```bash
    docker compose up -d
    ```

5. **Access the Application:**
    Open your browser and navigate to `https://app.carsties.com`.

## Media

### Home Page

![Screenshot 2024-07-02 230047](https://github.com/almoghindi/Carsties/assets/102804545/f3118070-6cc2-480e-86f4-51c1e60171a2)

### Car Page

![Screenshot 2024-07-02 230109](https://github.com/almoghindi/Carsties/assets/102804545/88b0e18e-229d-4a4f-8d24-1866834c1f4b)

---

This README provides a summary of the Carsties project, its features, the microservices architecture, the technologies used, and how to get started with the project.
