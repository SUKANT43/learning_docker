# Stage 1: Build the React app
FROM node:18 AS build

WORKDIR /app

# Copy only package.json to cache dependencies
COPY package.json package-lock.json* ./

RUN npm install

# Copy the rest of the project files
COPY . .

# Build the Vite app
RUN npm run build

# Stage 2: Serve with Nginx
FROM nginx:alpine

# Corrected path: /usr/share/nginx/html
COPY --from=build /app/dist /usr/share/nginx/html

# Expose port 80 for web traffic
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]

#docker 7
#docker run --name frontend  -p 8000:80 mern-frontend