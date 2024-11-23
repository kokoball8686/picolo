FROM node

RUN git clone https://github.com/gorisanson/pikachu-volleyball.git \
    && cd pikachu-volleyball \
    && npm install \
    && npm run build

EXPOSE 8080

CMD ["npx", "http-server", "dist"]

