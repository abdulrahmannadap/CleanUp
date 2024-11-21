Dukan/
│
├── Dukan.Application/                     # Application Layer (Use cases and application services)
│   ├── Services/                         # Application-specific services (business logic implementations)
│   │   ├── ProductService.cs             # Product-related application service
│   │   └── CategoryService.cs            # Category-related application service
│   ├── UseCases/                         # Use case classes (representing specific business tasks)
│   │   ├── GetProductByIdUseCase.cs      # Use case to fetch a product by ID
│   │   └── CreateCategoryUseCase.cs      # Use case to create a category
│   ├── Interfaces/                       # Interfaces defining the contracts for services
│   │   ├── IProductService.cs            # Interface for product services
│   │   └── ICategoryService.cs           # Interface for category services
│   ├── DTOs/                             # Data Transfer Objects for internal use
│   │   ├── ProductDto.cs                 # DTO for product data
│   │   └── CategoryDto.cs                # DTO for category data
│   └── Dukan.Application.csproj          # Project file for Application layer
│
├── Dukan.Domain/                          # Domain Layer (Business rules, entities, and domain logic)
│   ├── Entities/                         # Domain entities (e.g., business objects)
│   │   ├── Product.cs                    # Product entity representing product data
│   │   └── Category.cs                   # Category entity representing category data
│   ├── ValueObjects/                     # Value objects representing domain-specific concepts
│   │   ├── Price.cs                      # Value object for product price
│   │   └── Discount.cs                   # Value object for product discount
│   ├── Interfaces/                       # Interfaces defining domain services (repository contracts, etc.)
│   │   ├── IProductRepository.cs         # Interface for product repository data operations
│   │   └── ICategoryRepository.cs        # Interface for category repository data operations
│   └── Dukan.Domain.csproj               # Project file for Domain layer
│
├── Dukan.Infrastructure/                 # Infrastructure Layer (External dependencies and implementation details)
│   ├── Data/                             # Data access, repositories, database interactions
│   │   ├── EfProductRepository.cs        # EF implementation for product repository
│   │   └── EfCategoryRepository.cs       # EF implementation for category repository
│   ├── DukanDbContext.cs                 # DbContext for database interactions (EF)
│   └── Dukan.Infrastructure.csproj       # Project file for Infrastructure layer
│
├── Dukan.Presentation/                   # Presentation Layer (Console or Desktop UI layer)
│   ├── Services/                         # Service layer for interacting with application logic
│   │   ├── ProductDisplayService.cs      # Service to display product-related data
│   │   └── CategoryDisplayService.cs     # Service to display category-related data
│   ├── DukanApp.cs                       # Main application entry point (for console application)
│   ├── Models/                           # Internal models for interacting with UI
│   │   ├── ProductViewModel.cs           # ViewModel for product (display logic)
│   │   └── CategoryViewModel.cs          # ViewModel for category (display logic)
│   └── Dukan.Presentation.csproj         # Project file for Presentation layer
│
├── Dukan.Tests/                          # Unit tests for each layer
│   ├── ApplicationTests/                 # Tests for application layer (use cases, services)
│   │   ├── ProductServiceTests.cs        # Test for product service logic
│   │   └── CategoryServiceTests.cs       # Test for category service logic
│   ├── DomainTests/                      # Tests for domain layer (entities, value objects)
│   │   ├── ProductTests.cs               # Tests for product entity and logic
│   │   └── CategoryTests.cs              # Tests for category entity and logic
│   ├── InfrastructureTests/              # Tests for infrastructure layer (repositories, external services)
│   │   ├── EfProductRepositoryTests.cs   # Tests for EF product repository
│   │   └── EfCategoryRepositoryTests.cs  # Tests for EF category repository
│   └── Dukan.Tests.csproj                # Project file for Test layer
│
├── Dukan.sln                             # Solution file for Dukan solution
└── README.md                             # Project documentation, including setup, usage, and guidelines
