FROM nginx
RUN apt-get update
RUN apt-get -y install apt-utils npm
ADD Frontend /usr/share/nginx/html
RUN npm install --global yarn
RUN cd /usr/share/nginx/html && pwd && yarn install && yarn build
ENV NGINX_HOST=foobar.com
ENV NGINX_PORT=80
EXPOSE 80
CMD ["/usr/sbin/nginx"]
