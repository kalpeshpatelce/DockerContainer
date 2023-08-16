# DockerContainer
## Container for Microsoft SQL Server on Ubuntu
````
sudo docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Password@123" -p 1433:1433 -v /DB:/var/opt/mssql --name DBServer --hostname DBServer -d  mcr.microsoft.com/mssql/server:2019-latest
````
## Container with Mapped Data Directory
````
chmod 777 /DB

docker run -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=P@ssword@123' -e 'MSSQL_DATA_DIR=/DB' -v /DB:/DB --name DBServer --hostname DBServer -p 1433:1433 -d mcr.microsoft.com/mssql/server:2022-latest
````
