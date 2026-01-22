FROM node:20.20.0-alpine3.23
EXPOSE 8080
ENV DB_HOST=mysql
RUN addgroup -S expense && adduser -S expense -G expense
RUN mkdir /opt/server
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
CMD ["node", "index.js"]