
FROM ubuntu:22.04

RUN apt-get update && apt-get install -y ca-certificates libstdc++6

COPY --from=node:16-bullseye /usr/local /usr/local

WORKDIR /app

COPY package*.json ./

RUN npm install --legacy-peer-deps

COPY . .

RUN npm run build

RUN npm install -g serve@14

EXPOSE 5001

CMD ["serve", "-s", "-l", "5001", "build"]
