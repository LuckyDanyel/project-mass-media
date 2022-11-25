FROM node:18.12.1 as builder

WORKDIR /app

COPY Engine-search-service/ /app

RUN npm install && npm run build

FROM node:18.12.1 as production

COPY --from=builder app/package.json ./
COPY --from=builder app/dist ./dist

RUN npm install --omit=dev



