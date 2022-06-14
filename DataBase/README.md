# Configure the database

## Prerequisites

Docker should be installed.

## Deploy SQL Server image to Docker

* Pull and run the SQL Server Linux container image

    ```bash
    #!/bin/bash
    sudo docker pull mcr.microsoft.com/mssql/server:2022-latest
    ```

* To run the Linux container image with Docker, you can use the following command from a bash shell or elevated PowerShell command prompt.

    ```bash
    #!/bin/bash
    sudo docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=<YourStrong@Passw0rd>" \ -p 1433:1433 --name sql1 --hostname sql1 \ -d \ mcr.microsoft.com/mssql/server:2022-latest
    ```

## The second approach

```text
    Use Azure Data Studio to create a new SQL Server database and deploy it in Docker.
    Azure Data Studio is also powerful enough to create queries and run them in the database.
```

[Check out the Azure Data Studio quick start documentation](https://docs.microsoft.com/en-us/sql/azure-data-studio/quickstart-sql-server?view=sql-server-ver16)
