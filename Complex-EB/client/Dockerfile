# BUILD PHASE
FROM node:alpine as builder

WORKDIR '/app'

COPY package.json .

RUN npm install

COPY . .

RUN npm run build


# SECOND PHASE
FROM nginx
EXPOSE 3000
COPY --from=builder ./nginx/default.conf /etc/nginx/conf.d
COPY --from=builder /app/build /usr/share/nginx/html
