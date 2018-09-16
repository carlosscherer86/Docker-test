FROM microsoft/aspnetcore:2.0 AS base
WORKDIR /app
EXPOSE 80

FROM microsoft/aspnetcore-build:2.0 AS build
WORKDIR /src
COPY WebApplication13/WebApplication13.csproj WebApplication13/
RUN dotnet restore WebApplication13/WebApplication13.csproj
COPY . .
WORKDIR /src/WebApplication13
RUN dotnet build WebApplication13.csproj -c Release -o /app

FROM build AS publish
RUN dotnet publish WebApplication13.csproj -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "WebApplication13.dll"]
