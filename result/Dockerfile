FROM node:23-slim
WORKDIR /app
RUN apt update && apt install -y curl
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 80
CMD [ "npm", "start" ]