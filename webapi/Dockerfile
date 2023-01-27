FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS base
WORKDIR /app
EXPOSE 80

FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /src
COPY ["webapi/webapi.csproj", "src/webapi/"]
RUN dotnet restore "src/webapi/webapi.csproj" /bl
RUN echo "XXXXXXXXXXXXXXX"
RUN pwd

COPY *.binlog ~/Desktop/*.binlog
# COPY . .
# WORKDIR "/src/src/webapi"
# RUN dotnet build "webapi.csproj" -c Release -o /app/build

# FROM build AS publish
# RUN dotnet publish "webapi.csproj" -c Release -o /app/publish /p:UseAppHost=false

# FROM base AS final
# WORKDIR /app
# COPY --from=publish /app/publish .
# ENTRYPOINT ["dotnet", "webapi.dll"]