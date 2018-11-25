FROM node:8-slim
RUN apt-get update \
  && apt-get install -y --no-install-recommends graphicsmagick \
  && apt-get autoremove -y \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
WORKDIR /code
COPY package*.json ./
RUN npm install --production && npm ls
RUN mv ./node_modules /node_modules
COPY . .
EXPOSE 9000
CMD ["npm", "start"]

