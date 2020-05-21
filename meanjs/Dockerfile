FROM node:13.6.0-alpine

LABEL authors="narabel"

# 80 = HTTP, 443 = HTTPS, 3000 = MEAN.JS server, 35729 = livereload, 8080 = node-inspector
EXPOSE 80 443 3000 35729 8080

# Set development environment as default
ENV NODE_ENV development

RUN mkdir /opt/app
RUN chmod 777 -R /opt/app

RUN npm install --quiet -g yo generator-meanjs bower gulp node-pre-gyp mocha karma-cli pm2
# RUN npm cache clean 

RUN apk --no-cache add git

RUN apk --no-cache add python

RUN npm install --unsafe-perm -g node-sass

# RUN apk --no-cache add build-essential

# npm install generator-meanjs:crud-module
# npm rebuild node-sass

CMD ["node"]

