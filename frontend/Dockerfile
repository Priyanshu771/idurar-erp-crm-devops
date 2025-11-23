# --- Build Stage ---
FROM node:20-alpine AS build

WORKDIR /app

# Accept variables from docker-compose
ARG VITE_BACKEND_SERVER
ARG VITE_FILE_BASE_URL

# Pass ARG → ENV (Vite reads ENV)
ENV VITE_BACKEND_SERVER=$VITE_BACKEND_SERVER
ENV VITE_FILE_BASE_URL=$VITE_FILE_BASE_URL

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# --- Production Stage ---
FROM nginx:alpine

COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
