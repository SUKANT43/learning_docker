#use the ofiicial node.js image
FROM node:18


#set the working direcory in the container
WORKDIR /usr/src/app


#./ means we mentoning the above directoy as the path for it
COPY package.json ./ 
#this install the node modules that inside the package.json
RUN npm install
 
#the files copy from the backend folder to WORKDIR
COPY . .

#connecting our port and docker port
EXPOSE 5000

#command for running our server
CMD ["npm" ,"start"]

#docker build -t mern-backend . -t is for namming the container name is mern-backend and . is for current path

#docker run -p 5000:5000 mern-backend -p is for port mapping and mern-backend is the container name

#docker run --name mango -d -p 27017:27017 mongo :latest --name is for naming the container and -d is for running in detached mode and -

#docker network create mern-network this is for creating network combinnig the mongo and node in same server 

#docker run --name mongo --network mern-network -p 27017:27017 -d mongo running in a network


#docker run --name backend --network mern-network -p 5000:5000 mern-backend running our backend in a same network as same as mongo
