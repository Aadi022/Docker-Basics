#This dockerfile will pull image of nodejs and mongodb from dockerhub so that we can create nodejs and mongodb containers for our project
#using the nodejs image that is based on alpha linux distribution
FROM node:alpine  
#The WORKDIR /usr/src/app line sets the folder where the container will run its commands. 
WORKDIR /usr/src/app
#Copy packagelock and package to the directory. The dot in this command represents our working directory
COPY package*.json .
#Installing the dependencies mentioned in the packagelock and package. ci means continuous integration. RUN npm install would also work, but RUN npm ci is a better option
RUN npm ci
#Copy all the files present in our application to our working directory. Refer dockerignore for the files that should not be copied to the container.
COPY . .
#This command will be executed once my container starts
CMD npm start