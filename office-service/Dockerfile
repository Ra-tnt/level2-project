FROM node as sourcing

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY index.js /src/
COPY package*.json /src/

RUN cd /src && \
    npm install

FROM node
COPY --from=sourcing /src/node_modules /mynodeapp/node_modules

# bundle app source
COPY --from=sourcing /src/index.js /mynodeapp/
workdir /mynodeapp
CMD ["node","index.js"]



from node as build
copy index.js /src/
copy package* /src/
run cd /src && \
    npm install
from node
copy --from=build /src/node_modules /dist/node_modules/
copy index.js /dist/
workdir /dist
cmd ["node", "index.js"]

