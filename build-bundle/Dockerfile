FROM nginx:latest

RUN apt-get update && apt-get install -y less emacs-nox curl zsh

RUN mkdir /etc/nginx/tls/
COPY default.conf.template /etc/nginx/conf.d/

CMD  /bin/sh -c "envsubst < /etc/nginx/conf.d/default.conf.template > /etc/nginx/conf.d/default.conf && exec nginx-debug -g 'daemon off;'"

