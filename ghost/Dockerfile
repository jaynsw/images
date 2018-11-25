FROM node:10
WORKDIR /code
COPY package.json ./package.json
RUN yarn --pure-lockfile
RUN mv ./node_modules /node_modules
EXPOSE 9000
CMD ["npm", "start"]

