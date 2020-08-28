FROM postman/newman:alpine

# working directory for Newman commands and our scripts
WORKDIR /etc/newman

# copy over my app package.json
COPY ./app/package*.json ./

# install app
RUN npm ci

# Bundle app source
COPY ./app/app.js ./

ENTRYPOINT ["npm", "run", "start"]

