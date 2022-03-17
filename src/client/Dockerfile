FROM node:9 AS build
WORKDIR /app
ADD package.json .
RUN npm install

FROM node:9-slim
COPY --from=build /app .
ADD . .
EXPOSE 3000
CMD ["node", "index.js"]
