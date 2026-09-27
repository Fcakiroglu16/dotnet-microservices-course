# .NET Microservices Course

Course repository showing asynchronous communication between independent .NET services over a message broker.

## Services

| Service | Role |
|---|---|
| `One.API` | Publishes `UserCreatedEvent` |
| `Two.API` | Consumes `UserCreatedEvent` |
| `NotificationWorkerService` | Background worker consuming the same event |
| `SharedLibrary` | Shared event contracts |

## Topics Covered

- Service boundaries and shared contract libraries
- Publish/subscribe messaging between services
- Event consumers in both an API and a worker service
- Containerizing services with Docker

## Getting Started

```bash
git clone https://github.com/Fcakiroglu16/dotnet-microservices-course.git
cd dotnet-microservices-course

dotnet run --project One.API
dotnet run --project Two.API
dotnet run --project NotificationWorkerService
```

A running message broker is required; configure its connection in each service's `appsettings.json`.

## Requirements

- .NET SDK
- Docker (for the broker and container builds)
