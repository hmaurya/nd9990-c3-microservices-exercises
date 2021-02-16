# Use NodeJS base image
FROM node:13

RUN apt-get update && apt-get install -y unzip zip

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy app source
COPY . .

# Build prod
RUN npm run build

# Bind the port that the image will run on
EXPOSE 8080

ENV POSTGRES_USERNAME=udagramhmauryadev
ENV POSTGRES_PASSWORD=p2udagram
ENV POSTGRES_HOST=udagramhmauryadev.cjnng5rhulgd.us-east-2.rds.amazonaws.com
ENV POSTGRES_DB=udagramhmauryadev
ENV AWS_BUCKET=udacity-website-hmaurya
ENV AWS_REGION=us-east-2
ENV AWS_PROFILE=default
ENV JWT_SECRET=helloworld
ENV URL=http://localhost:8100

# Define the Docker image's behavior at runtime
CMD ["node", "www/server.js"]
