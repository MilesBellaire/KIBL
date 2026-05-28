# KIBL

![KIBL Logo](./Logo.png)

KIBL is a comprehensive pet care platform designed to help pet owners make informed decisions about pet food products. The platform analyzes products based on animal-specific factors to determine suitability for dogs and cats.

## Architecture

KIBL is built as a microservice architecture with three distinct services:

```
KIBL/
├── KIBL-algorithm/    # gRPC-based product analysis service
├── KIBL-backend/      # ASP.NET Core 8.0 REST API
└── KIBL-frontend/     # React Native mobile application
```

### Service Overview

| Service | Purpose | Technology |
|---------|---------|------------|
| **KIBL-algorithm** | Analyzes pet food products using gRPC for ingredient and nutritional analysis | Python, gRPC, Protocol Buffers |
| **KIBL-backend** | RESTful API providing authentication, user management, product catalog, and more | ASP.NET Core 8.0, MySQL, Entity Framework Core |
| **KIBL-frontend** | Cross-platform mobile app for users to browse products, scan barcodes, and view analysis | React Native, Expo, Redux Toolkit |

## Why Microservices?

This project was developed as a student project, and we chose a microservice architecture primarily for organizational purposes. The sectioned-off nature of microservices helped us:

- Keep different concerns (algorithm, API, UI) clearly separated
- Manage dependencies and complexity in a learning environment
- Practice distributed system concepts
- Make each service more manageable and understandable

While we could have used a monolithic approach, the microservice structure provided a cleaner separation of concerns that was beneficial for learning distributed system design.

## Features

- **Product Analysis** - Get detailed safety scores and ingredient analysis for pet food products
- **Animal-Specific Analysis** - Tailored recommendations for dogs and cats based on breed, weight, and medical conditions
- **Barcode Scanning** - Scan product barcodes to instantly get product details and analysis
- **Pet Profiles** - Create and manage pet profiles with dietary preferences
- **Product Catalog** - Browse and search through pet products
- **Reviews & Ratings** - Community-driven reviews and ratings
- **Saved Products** - Save favorite products for quick access
- **Vet Information** - Find and browse vet clinic information

## Getting Started

Each service has its own README with setup instructions:

- [KIBL-algorithm README](https://github.com/milesbellaire/KIBL-algorithm) - Set up and run the analysis service
- [KIBL-backend README](https://github.com/milesbellaire/KIBL-backend) - Set up and run the REST API backend
- [KIBL-frontend README](https://github.com/milesbellaire/KIBL-frontend) - Build and run the mobile application

### Prerequisites

- **Algorithm Service**: Python 3.x
- **Backend**: .NET 8.0 SDK, MySQL 8.0+
- **Frontend**: Node.js 18+, Expo CLI

## Project Structure

```
KIBL/
├── KIBL/                 # Main repository
├── KIBL-algorithm/       # Product analysis microservice
├── KIBL-backend/         # REST API microservice
└── KIBL-frontend/        # Mobile application
```

## Technology Stack

- **Frontend**: React Native, Expo, Redux Toolkit
- **Backend**: ASP.NET Core 8.0, Entity Framework Core, MySQL
- **Algorithm**: Python, gRPC, Protocol Buffers
