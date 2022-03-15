FROM node:alpine as builder
WORKDIR /app

COPY ./sowt-app .
RUN npm install
RUN npm run build
 
FROM nginx:alpine
RUN rm -rf /usr/share/nginx/html/*
COPY --from=builder /app/build /usr/share/nginx/html
RUN rm /etc/nginx/nginx.conf 
COPY nginx.conf /etc/nginx/nginx.conf

   

EXPOSE 8081
