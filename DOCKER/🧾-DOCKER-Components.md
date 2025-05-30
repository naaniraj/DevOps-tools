## DOCKER-COMPNENTS
*******************************
1. FROM – Base Image<br>
Specifies the base image to use (required).<br>
EX : FROM python:3.10<br>

2. LABEL – Metadata<br>
Adds metadata like the author, version, etc.<br>
EX : LABEL maintainer="niranjan@example.com"<br>

3. RUN – Execute Commands During Build<br>
Executes commands while building the image.<br>
EX: RUN apt-get update && apt-get install -y nginx<br>

4. COPY – Copy Files from Host<br>
Copies files/folders from your machine into the image.<br>
EX:COPY . /app<br>

5. ADD – Similar to COPY (but can also handle URLs and auto-extract tar files)<br>
ADD https://example.com/file.tar.gz /app/<br>

6. WORKDIR – Set Working Directory<br>
Sets the working directory for the container.<br>
EX : WORKDIR /app<br>

7. ENV – Environment Variables<br>
Sets environment variables.<br>
EX:ENV PORT=8080<br>

8. EXPOSE – Inform Docker About Ports<br>
Documents which ports will be used.<br>
EX: EXPOSE 5000<br>

9. CMD – Default Command (can be overridden)<br>
What to run by default when the container starts.<br>
EX: CMD ["python", "app.py"]<br>

10. ENTRYPOINT – Define a Fixed Command<br>
Similar to CMD, but harder to override.<br>
EX: ENTRYPOINT ["python", "app.py"]<br>

11. VOLUME – Mount Host Directory<br>
Creates a mount point with a volume.<br>
EX: VOLUME ["/data"]<br>

🔁 Example Dockerfile
_________________________

dockerfile<br>
Copy<br>
Edit<br>
FROM node:18<br>
WORKDIR /app<br>
COPY . .<br>
RUN npm install<br>
EXPOSE 3000<br>
CMD ["npm", "start<br>

## DOCKER COMPONENTS IN SIMPLE 
**********************************
***DOCKER FILE COMPONENTS:***<br>
FROM: THIS COMPONENT IS USED TO DEFINE BASE IMAGES (ubuntu, centos, httpd, jenkins)<br>
MAINTAINER: THIS IS USED TO ADD AUTHOR DETAILS <br>
LABEL: IT IS USED TO ADD A DESCRIPTION FOR OUR IMAGE<br>
COPY: USED TO COPY THE FILES FROM HOST TO CONTAINER<br>
ADD: USED TO COPY THE FILES FROM HOST TO CONTAINER AND ALSO IT WILL DOWNLOAD THE FILES FROM IE AND SEND THOSE FILES TO CONTAINER.<br>
RUN: IS USED TO EXECUTE THE COMMANDS, WHILE CREATING AN IMAGE<br>
CMD: IS USED TO EXECUTE THE COMMANDS, WHILE CREATING A CONTAINER<br>
ENTRYPOINT: IS USED TO EXECUTE THE COMMANDS, WHILE CREATING A CONTAINER, IT <br>
HAS HIGH PRIORITY THAN CMD AND ALSO IT WILL OVERWRITE THE VALUES OF CMD<br>
ENV: IS USED TO DEFINE THE VARS, IT IS NOT POSSIBLE TO PASS THE VALUES <br>
DYNAMICALLY. WE CAN ACCESS THOSE VARS IN CONTAINER<br>
ARG: IS USED TO DEFINE THE VARS, IT IS POSSIBLE TO PASS THE VALUES. DYNAMICALLY. <br>
WE CAN’T ACCESS THOSE VARS IN CONTAINER.<br>
WORKDIR: USED TO SET A DEFAULT PATH IN CONTAINER<br>
EXPOSE: USED TO DEFINE CONTAINER PORTS<br>

