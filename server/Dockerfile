FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy only backend-relevant files
COPY package.json ./
COPY package-lock.json ./
COPY index.js ./

# Install dependencies
RUN npm install

# Expose backend port
EXPOSE 3000

# Start the app
CMD ["node", "index.js"]
