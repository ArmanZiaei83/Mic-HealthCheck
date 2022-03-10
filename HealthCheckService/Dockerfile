FROM mcr.microsoft.com/dotnet/sdk:5.0 AS builder
WORKDIR /src
COPY HealthCheckService.csproj .
RUN dotnet restore "HealthCheckService.csproj"
COPY . .
RUN dotnet publish -c Release -o publish

FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
WORKDIR /app
COPY --from=builder /src/publish .
EXPOSE 80
ENTRYPOINT ["dotnet", "HealthCheckService.dll"]