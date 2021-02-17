# Use NodeJS base image
FROM node:13

ENV POSTGRES_USERNAME=udagramhmauryadev
ENV POSTGRES_PASSWORD=p2udagram
ENV POSTGRES_HOST=udagramhmauryadev.cjnng5rhulgd.us-east-2.rds.amazonaws.com
ENV POSTGRES_DB=udagramhmauryadev
ENV AWS_BUCKET=udacity-website-hmaurya
ENV AWS_REGION=us-east-2
ENV AWS_PROFILE=default
ENV JWT_SECRET=helloworld
ENV PORT=8080
ENV URL=http://localhost:${PORT}

# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./
RUN npm ci

# Bundle app source
COPY . .

EXPOSE 8080

CMD [ "npm", "run", "prod" ]



