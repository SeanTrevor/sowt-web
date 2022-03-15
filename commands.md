# Docker Commands

### For sowt.ca
- Lists all containers
> sudo docker container ls -a

- Create container image for sowt.ca
> sudo docker build -t webserver .

- Create container for production sowt.ca
> sudo docker run --restart=unless-stopped -it -d -p 80:80 --name web webserver

- Create container for development
> sudo docker run -it --rm -d -p 8080:81 --name web-dev -v ~/projects/sowt_web/src:/usr/share/nginx/html-dev webserver

- Stop and remove container named web
> sudo docker stop web
> sudo docker rm web

- Remove all containers 
> sudo docker rm -f $(sudo docker ps -aq)
