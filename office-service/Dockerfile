FROM node

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY index.js ./
COPY package*.json ./

RUN npm install

# bundle app source
COPY . .

CMD ["node","index.js"]

