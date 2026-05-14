FROM node:20-alpine
WORKDIR  /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 5173

# can add --port 3000 for app to run on port 3000 of the container
CMD ["npm", "run", "dev","--","--host"]  

# to build an image run: -t gives the name for image
# docker build -t client .

# create a container and run the image
# docker run -d -p <host-port>:<container-port> --name <container-name> <image-name>
# docker run -d -p 5173:5173 --name client-container client

# we access the app thru host ports if it was -p 8080:5173 we will go to localhost:8080 to access the app
