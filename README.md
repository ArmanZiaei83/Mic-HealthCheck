# Mic-HealthCheck
This project is a simple example of health check microservice for showing liveness and readiness of other microservices.
Health check is a real important thing in any cloud native environment.
In this case I've used  <a href="https://www.nuget.org/packages/Microsoft.Extensions.Diagnostics.HealthChecks/">Microsoft.Extensions.Diagnostics.HealthChecks.EntityFrameworkCore</a> NuGet package.

## How To Use
- This project has been dockerized, so the first necessary things is to have Docker installed on your OS.
- just navigate into <code>project-dir/HealthCheckService</code> and execute docker-compose build then docker-compose up.

## Adding New Services For Health Checking
if you have other services for health checking, you have to write their docker host address in </br><code>project-dir/HealthCheckService/appsettings.json</code> file and set their names.
