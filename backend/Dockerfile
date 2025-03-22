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