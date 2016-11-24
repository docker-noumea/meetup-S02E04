FROM microsoft/dotnet:1.0.1-sdk-projectjson

ENV ASPNETCORE_ENVIRONMENT="Development"

COPY . /app

WORKDIR /app

RUN ["dotnet", "restore"]

RUN ["dotnet", "build"]

RUN ["dotnet", "ef", "database", "update"]

EXPOSE 5000/tcp

ENTRYPOINT ["dotnet", "run", "--server.urls", "http://*:5000"]