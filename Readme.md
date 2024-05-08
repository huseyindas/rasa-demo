Rasa X Installation and Configuration
This README file provides a step-by-step guide to install Rasa X and perform necessary configurations.

Step 1: Installation and Build with Docker
First, install Rasa X using Docker. Run the following command to start Rasa X in Docker:

```sh
docker-compose up --build -d
```
This command will build and run Rasa X.

Step 2: Permission Settings
After installation with Docker compose, it's important to set the necessary permissions. You can use the following command to set permissions for the ./rasa directory:

```bash
sudo chgrp -R root ./* && sudo chmod -R 770 ./*
```
However, you might need to correct permissions for the ./db directory. In that case, you can use the following commands to set the correct permissions:

```bash
sudo chown -R 1001 ./db && sudo chmod -R 750 ./db
```
If you are mounting different or extra directories, please adapt their permissions accordingly.

Step 3: Postgres Database Settings
To configure the database storage for Rasa X, follow these steps:

For Linux Users:
A local directory is used for persistent Postgres database storage. You can set the owner and permissions of the database persistence directory using the following command:
```bash
sudo chown -R 1001 ./db && sudo chmod -R 750 ./db
```
After following these steps, you can start Rasa X using the following command:

```bash
sudo docker-compose up -d
```
This command will start Rasa X in the background.