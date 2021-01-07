FROM node:latest
EXPOSE 80

ENV APP_ROOT /app
RUN mkdir $APP_ROOT
WORKDIR $APP_ROOT

COPY package*.json /
COPY . /

RUN npm install
CMD ["npm", "run", "dev"]
