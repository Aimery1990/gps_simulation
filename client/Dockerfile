# Stage 1: Build the React frontend with Vite
FROM node:20-alpine AS build

WORKDIR /app

# Step 1: Copy package files and install dependencies
COPY package.json package-lock.json ./
RUN npm install

# Step 2: Copy the rest of the app and build
COPY . .
RUN npm run build

# Stage 2: Serve with nginx
FROM nginx:alpine

COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
