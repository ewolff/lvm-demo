FROM node:6.9.1-alpine
RUN apk update && apk upgrade
RUN apk add git curl openssh
RUN rm -rf /var/cache/apk/*
RUN git clone https://github.com/ewolff/roca-las-damage.git
RUN cd roca-las-damage && npm install
RUN cd roca-las-damage && npm run compile
CMD cd roca-las-damage && npm run server
EXPOSE 3003