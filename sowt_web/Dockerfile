FROM nginx:latest
RUN rm /etc/nginx/nginx.conf

COPY ./src /usr/share/nginx/html/
COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 8080
