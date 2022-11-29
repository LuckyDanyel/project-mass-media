FROM node:18.12.1 as builder

WORKDIR /app

COPY Engine-search-service/ /app

RUN npm install
RUN npm run build

FROM node:18.12.1 as production

WORKDIR /app

COPY --from=builder app/package.json app/
COPY --from=builder app/dist app/dist

RUN npm install --omit=dev



