
**Remarks**

- This docker compose setup is intended to be a simple example of developing local applications in Django without the need to install anything other than Docker and Docker compose on the system.

- docker-compose.dev.yml is configured to mount the project folder baseProject as a volume in the container in order to synchronize file changes to allow automatic restart of the runserver avoiding the need to build the image for each change

- docker-compose.dev.yml is configured to mount the database data folder as a volume in the container in order to keep changes to the development database even if the containers are recreated



## Docker compose development
1. Go to docker folder
2. Set up environment
   1. Set up build environment
      - create .env file at the docker folder, the same folder where docker-compose.dev.yml is located
      - add required variables to .env file like the example below:
      ```
      DATABASE_NAME=baseProject
      DATABASE_USER=baseProject
      DATABASE_PASSWORD=baseProject
      DATABASE_HOST=db
      DATABASE_PORT=5432
      ```

3. Build docker compose
   ```
   docker-compose build
   ```
4. Start docker compose
   ```
   docker-compose up
   ```
   
### Commands


   ```
   docker-compose run baseProject python manage.py migrate
   ```
