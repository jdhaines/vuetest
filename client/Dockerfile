# Build
FROM node:alpine as build-stage
WORKDIR /app
COPY package*.json ./
RUN npm install --production
COPY . .
# RUN npm run serve
# EXPOSE 8080
CMD ["npm", "run", "serve"]

# Show
# FROM nginx:alpine as production-stage
# COPY --from=build-stage /app/dist /usr/share/nginx/html
# CMD ["nginx", "-g", "daemon off;"]