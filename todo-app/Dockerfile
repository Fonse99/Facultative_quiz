# #STAGE: building stage
# FROM node:10.19.0 as build

# ARG API_HOST

# WORKDIR /usr/src/app

# COPY . ./

# RUN npm install

# RUN REACT_APP_API_URL=${API_HOST} npm run build

#STAGE: production stage
FROM nginx:latest

COPY ./build ./usr/share/nginx/html

EXPOSE 80

CMD [ "nginx", "-g", "daemon off;" ]