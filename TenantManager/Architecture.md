Normal 
src/
├── app.module.ts               # Root module
├── main.ts                     # Entry point of the application
├── common/                     # Shared utilities and modules
│   ├── decorators/             # Custom decorators
│   ├── dtos/                   # Data Transfer Objects (DTOs)
│   ├── exceptions/             # Custom exceptions
│   ├── filters/                # Exception filters
│   ├── guards/                 # Authorization guards
│   ├── interceptors/           # Interceptors
│   ├── interfaces/             # Shared interfaces
│   ├── middlewares/            # Middleware
│   └── pipes/                  # Validation and transformation pipes
├── config/                     # Configuration files
│   ├── app.config.ts           # General application config
│   ├── database.config.ts      # Database configuration
│   └── env/                    # Environment-based configurations
├── modules/                    # Application modules
│   ├── auth/                   # Authentication module
│   │   ├── auth.controller.ts  # Auth controller
│   │   ├── auth.service.ts     # Auth service
│   │   ├── auth.module.ts      # Auth module
│   │   ├── dtos/               # DTOs specific to auth
│   │   └── strategies/         # Auth strategies (e.g., JWT, Passport)
│   ├── users/                  # Users module
│   │   ├── users.controller.ts # Users controller
│   │   ├── users.service.ts    # Users service
│   │   ├── users.module.ts     # Users module
│   │   └── dtos/               # DTOs specific to users
│   └── ...                     # Additional modules
├── database/                   # Database setup
│   ├── entities/               # Database entities
│   ├── migrations/             # Migration files
│   └── seeds/                  # Seed data
├── utils/                      # Helper utilities
│   ├── logger.util.ts          # Logging utility
│   └── ...                     # Additional utilities
└── tests/                      # Tests
    ├── e2e/                    # End-to-end tests
    └── unit/                   # Unit tests


Hexagonal

src/
├── app.module.ts                 # Root application module
├── main.ts                       # Application entry point
├── core/                         # Business logic (core domain)
│   ├── entities/                 # Domain entities
│   ├── services/                 # Business logic (use cases)
│   ├── ports/                    # Interfaces for incoming and outgoing interactions
│   └── exceptions/               # Domain-specific exceptions
├── application/                  # Application layer
│   ├── dtos/                     # Data Transfer Objects
│   ├── use-cases/                # Application-specific use cases
│   ├── facades/                  # Application-facing APIs for orchestrating the core
│   └── validators/               # Validation logic
├── infrastructure/               # External dependencies and framework-specific code
│   ├── database/                 # Database-related implementations
│   │   ├── orm/                  # ORM configuration
│   │   ├── entities/             # ORM-specific entities
│   │   ├── repositories/         # Database repositories (implements core ports)
│   │   └── migrations/           # Database migrations
│   ├── controllers/              # HTTP controllers (implements application ports)
│   ├── adapters/                 # Adapters for external APIs, services, etc.
│   ├── middlewares/              # Application middlewares
│   └── config/                   # Application configuration files
├── shared/                       # Shared utilities and abstractions
│   ├── constants/                # Application constants
│   ├── utils/                    # Helper functions and utilities
│   ├── logger/                   # Logging utility
│   └── ...                       # Other shared resources
├── tests/                        # Test files
│   ├── e2e/                      # End-to-end tests
│   └── unit/                     # Unit tests


