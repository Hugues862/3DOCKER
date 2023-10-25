# Use the official Microsoft .NET Core runtime image
FROM mcr.microsoft.com/dotnet/runtime:7.0 AS base
WORKDIR /app

FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /src
COPY ["Worker.csproj", "./"]
RUN dotnet restore "Worker.csproj"
COPY . .
RUN dotnet publish "Worker.csproj" -c release -o /app/publish --no-restore

FROM base AS final
WORKDIR /app
COPY --from=build /app/publish .
ENTRYPOINT ["dotnet", "Worker.dll"]
