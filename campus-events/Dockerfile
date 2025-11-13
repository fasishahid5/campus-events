FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install -g parcel http-server

COPY . .

# Build HTML with Parcel
RUN parcel build src/index.html

EXPOSE 8080

CMD ["http-server", "dist", "-p", "8080"]
