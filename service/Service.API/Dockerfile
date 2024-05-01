FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS base
WORKDIR /app
EXPOSE 8080

FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src
COPY ["./Service.API.csproj", "./"]
RUN dotnet restore "./Service.API.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "Service.API.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Service.API.csproj" -c Release -o /app/publish /p:UseAppHost=false

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Service.API.dll"]