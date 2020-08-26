FROM node as sourcing

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY index.js /src/
COPY package*.json /src/

RUN cd /src && \
    npm install

FROM node
COPY --from=sourcing /src/node_modules /mynodeapp/node_modules && \
     /src/index.js /mynodeapp/
workdir /mynodeapp
CMD ["node","index.js"]
