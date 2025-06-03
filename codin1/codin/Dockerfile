FROM node:20-alpine AS development
ENV NODE_ENV=development
WORKDIR /lopez_laura_site    
COPY package.json ./
COPY yarn.lock ./
RUN yarn install 
COPY . .
EXPOSE 7775
CMD [ "yarn", "dev"]

FROM node:20-alpine AS builder
WORKDIR /lopez_laura_site
COPY . .
RUN yarn install
RUN yarn build

FROM nginx:1.21.0-alpine AS production
COPY --from=builder /lopez_laura_site/dist /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 7775
CMD ["nginx", "-g", "daemon off;"]