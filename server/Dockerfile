FROM node:alpine

WORKDIR '/app'

# directorio actual directorio destino
COPY ./package.json ./

# Install dependencias
RUN npm install

COPY . .

CMD ["npm","run","start"]

## docker build -f Dockerfile.dev  -t valvarezxxx/server . 
### docker run valvarezxxx/server