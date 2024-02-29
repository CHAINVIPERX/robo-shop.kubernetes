FROM node:18.19.1-alpine3.19
EXPOSE 8080
ENV MONGO=true

WORKDIR /opt/server
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
RUN chown roboshop:roboshop /opt/server
USER roboshop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
RUN echo "Hello!"
CMD [ "node", "server.js" ]