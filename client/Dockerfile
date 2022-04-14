# uso version antigua de node xq mi proyecto cliente esta crado con una version antigua de react, de lo contrario error
FROM node:14.14.0-alpine as builder
WORKDIR '/app'
# directorio actual directorio destino
COPY ./package.json ./
# Install dependencias
RUN npm install
COPY . .
RUN npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
# Copio los archivos de la fase de cosntruccion
COPY --from=builder /app/build /usr/share/nginx/html


## docker build -f Dockerfile.dev  -t valvarezxxx/client . 
### docker run valvarezxxx/client