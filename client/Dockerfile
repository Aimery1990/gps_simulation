# Stage 1: Build Vite React app
FROM node:18-alpine AS build

WORKDIR /app

# Step 1: Copy only package files and install deps (uses cache better)
COPY package.json package-lock.json ./
RUN npm install

# Step 2: Copy the rest of the app and build
COPY . .
RUN npm run build

# Stage 2: Serve with nginx
FROM nginx:alpine

# Copy built files from previous stage
COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
