# Mic-HealthCheck
This project is a dockerized application that can be used for showing liveness and readiness of other microservices.
Health check is a real important concept in any cloud native infrastructure.
In this case I've used  <a href="https://www.nuget.org/packages/Microsoft.Extensions.Diagnostics.HealthChecks/">Microsoft.Extensions.Diagnostics.HealthChecks.EntityFrameworkCore</a> NuGet package.

## How To Use
- This project has been dockerized, so the first necessary thing is to have Docker installed on your OS.
- just navigate into <code>project-dir/HealthCheckService</code> and execute docker-compose build then docker-compose up.

## Adding New Services For Health Checking
If you have other services for health checking, write their docker host address in </br><code>project-dir/HealthCheckService/appsettings.json</code> file and set their names.
