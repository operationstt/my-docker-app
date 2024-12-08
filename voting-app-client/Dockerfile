# Use Node.js as the base
FROM node:20-alpine

#Install curl
RUN apk add --no-cache curl

WORKDIR /app

COPY . . 

RUN npm install

RUN IP=$(curl -s curl ifconfig.me) && \
  echo "REACT_APP_BACKEND_API_URL=$IP">.env

EXPOSE 3001

CMD ["npm", "start"]
