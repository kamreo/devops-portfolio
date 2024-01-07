FROM mcr.microsoft.com/dotnet/aspnet:latest AS base
WORKDIR /app
EXPOSE 80

FROM mcr.microsoft.com/dotnet/sdk:latest AS build
WORKDIR /src
COPY ["EscapadezApi.csproj", "./"]
RUN dotnet restore "./EscapadezApi.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "EscapadezApi.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "EscapadezApi.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "EscapadezApi.dll"]
