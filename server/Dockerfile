FROM node:18-alpine

WORKDIR /app

# Copy backend dependencies from root
COPY ../package.json ../package-lock.json ./

# Copy backend source code
COPY . .

RUN npm install

EXPOSE 3000

CMD ["node", "server.js"]
