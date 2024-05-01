FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS base
WORKDIR /app
EXPOSE 8080

FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src
COPY ["./Yarp.Gateway.csproj", "./"]
RUN dotnet restore "./Yarp.Gateway.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "Yarp.Gateway.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Yarp.Gateway.csproj" -c Release -o /app/publish /p:UseAppHost=false

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Yarp.Gateway.dll"]