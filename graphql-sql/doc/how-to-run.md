# How to run

- README通りにやっても動かないので、以下のように修正する

> ref: <https://keploy.io/docs/server/macos/installation/>

## create testcase

```bash
# up keploy
keploy record -c "docker build . -t graphql-sql-app && docker run -p 8080:8080 --name graphql-sql-app-1 --network keploy-network  graphql-sql-app" --containerName "graphql-sql-app-1" --delay 10

```

## run testcase

```bash
keploy test -c "docker build . -t graphql-sql-app && docker run -p 8080:8080 --name graphql-sql-app-1 --network keploy-network  graphql-sql-app" --containerName "graphql-sql-app-1" --delay 10

``
