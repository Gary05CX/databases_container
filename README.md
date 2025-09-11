# Database Testing Environment
This project sets up a local environment for testing and demo purposes using Docker containers for PostgreSQL and MongoDB databases.
## Important Notice
**This container setup is strictly for testing or demo purposes only. It is not intended for deployment in any real services due to potential bugs or security issues.**
# Database Connection Details
### PostgreSQL
- **Username**: postgres
- **Password**: postgres
- **Localhost Port**: 6534
### MongoDB
- **Localhost Port**: 27170
# Usage
1. Ensure you have Docker and Docker Compose installed.
2. Open a terminal in this directory.
3. Run `docker compose up`.
4. Use `CTRL+C` or `control + C` to stop the container when you are finished using it.
## MongoDB
#### Connect via MongoDB Compass
1. Ensure you have MongoDB and MongoDB Compass installed.
2. Open a browser.
3. Type `mongodb://localhost:27170` and open it via MongoDB Compass.
4. The database of `localhost:27170` should appear. Click it. 
5. Click `Open MongoDB shell`.
#### Connect in Docker
1. Open Docker Desktop.
2. Go to the container tap.
3. Open the images of this container by clicking the ">" button.
4. Click MongoDB_Server. 
5. Click `Exce`tap and run your MongoDB command by starting with `mongosh`. 
#### Connect by local terminal
1. Ensure you have MongoDB installed.
2. Open your terminal.
3. Run `mongosh --port 27170` and start using.
## PostgreSQL
#### Connect via pgAdmin4
1. Ensure you have PostgreSQL and pgAdmin4 installed.
2. Open your pgAdmin4.
3. Right-click `Server`.
4. `Register` > `Server`.
5. Customise a name yourself.
6. Get into `Connection` and set it like below.
	- **Host name/address**: localhost
	- **Port**: 6543
	- **Maintenance database**: postgres
	- **Username**: postgres
	- **Password**: postgres
7. A database server named by you should appear. 
#### Connect in Docker
1. Open Docker Desktop.
2. Go to the container tap.
3. Open the images of this container by clicking the ">" button.
4. Click PostgreSQL_Server. 
5. Click `Exce`tap and run your PostgreSQL command by starting with the command below.
```
psql -h localhost -d postgres -U postgres
```
#### Connect by local terminal
1. Ensure you have PostgreSQL installed.
2. Open your terminal.
3. Run `psql -h localhost -p 6543 -d postgres -U postgres` and start using.
# Database log storage
After you run this container, a `.database` directory should be created under this project directory. This folder contains the data files and log files of both 2 databases.