# Base Image
FROM node:20

# Working directory inside app
WORKDIR /app

# copy package json inside docker
COPY package*.json ./

# Run npm install command
RUN npm install
# copy the working directory inside the container
COPY . .

# Run build command to check if the app is production ready
Run npm run build

# Expose the port so that we can access it from outside
EXPOSE 5173

# start command
CMD [ "npm","run", "dev" ]