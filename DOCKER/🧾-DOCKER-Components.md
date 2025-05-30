## DOCKER-COMPNENTS
*******************************
1. FROM – Base Image
Specifies the base image to use (required).
EX : FROM python:3.10

2. LABEL – Metadata
Adds metadata like the author, version, etc.
EX : LABEL maintainer="niranjan@example.com"

3. RUN – Execute Commands During Build
Executes commands while building the image.
EX: RUN apt-get update && apt-get install -y nginx

4. COPY – Copy Files from Host
Copies files/folders from your machine into the image.
EX:COPY . /app

5. ADD – Similar to COPY (but can also handle URLs and auto-extract tar files)
ADD https://example.com/file.tar.gz /app/

6. WORKDIR – Set Working Directory
Sets the working directory for the container.
EX : WORKDIR /app

7. ENV – Environment Variables
Sets environment variables.
EX:ENV PORT=8080

8. EXPOSE – Inform Docker About Ports
Documents which ports will be used.
EX: EXPOSE 5000

9. CMD – Default Command (can be overridden)
What to run by default when the container starts.
EX: CMD ["python", "app.py"]

10. ENTRYPOINT – Define a Fixed Command
Similar to CMD, but harder to override.
EX: ENTRYPOINT ["python", "app.py"]

11. VOLUME – Mount Host Directory
Creates a mount point with a volume.
EX: VOLUME ["/data"]

🔁 Example Dockerfile
_________________________

dockerfile
Copy
Edit
FROM node:18
WORKDIR /app
COPY . .
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]

## DOCKER COMPONENTS IN SIMPLE 
**********************************
DOCKER FILE COMPONENTS:
FROM: THIS COMPONENT IS USED TO DEFINE BASE IMAGES (ubuntu, centos, httpd, jenkins)
MAINTAINER: THIS IS USED TO ADD AUTHOR DETAILS 
LABEL: IT IS USED TO ADD A DESCRIPTION FOR OUR IMAGE
COPY: USED TO COPY THE FILES FROM HOST TO CONTAINER
ADD: USED TO COPY THE FILES FROM HOST TO CONTAINER AND ALSO IT WILL DOWNLOAD THE FILES FROM IE AND SEND THOSE FILES TO CONTAINER.
RUN: IS USED TO EXECUTE THE COMMANDS, WHILE CREATING AN IMAGE
CMD: IS USED TO EXECUTE THE COMMANDS, WHILE CREATING A CONTAINER
ENTRYPOINT: IS USED TO EXECUTE THE COMMANDS, WHILE CREATING A CONTAINER, IT 
HAS HIGH PRIORITY THAN CMD AND ALSO IT WILL OVERWRITE THE VALUES OF CMD
ENV: IS USED TO DEFINE THE VARS, IT IS NOT POSSIBLE TO PASS THE VALUES 
DYNAMICALLY. WE CAN ACCESS THOSE VARS IN CONTAINER
ARG: IS USED TO DEFINE THE VARS, IT IS POSSIBLE TO PASS THE VALUES. DYNAMICALLY. 
WE CAN’T ACCESS THOSE VARS IN CONTAINER.
WORKDIR: USED TO SET A DEFAULT PATH IN CONTAINER
EXPOSE: USED TO DEFINE CONTAINER PORTS

