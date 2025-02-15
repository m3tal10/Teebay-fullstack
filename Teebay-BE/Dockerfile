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
# run pre start commands
RUN npx prisma generate
# Run build command to check if the app is production ready
RUN npm run build
# Expose the port so that we can access it from outside
EXPOSE 5000

# start command
CMD npx prisma migrate deploy && npm run dev