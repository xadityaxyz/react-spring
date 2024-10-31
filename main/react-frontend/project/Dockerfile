# Use Node image to build the React app
FROM node:16-alpine AS build
WORKDIR /app
COPY react-frontend/project /app
RUN npm install && npm run build

# Use Nginx to serve the static files
FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 3000
CMD ["nginx", "-g", "daemon off;"]
