FROM node:6.9.1-alpine
RUN apk update && apk upgrade
RUN apk add git curl openssh
RUN rm -rf /var/cache/apk/*
RUN git clone https://github.com/LVM-IT/roca-las.git
RUN cd roca-las && npm install
RUN cd roca-las && npm run compile
CMD cd roca-las && npm run server
EXPOSE 3000
