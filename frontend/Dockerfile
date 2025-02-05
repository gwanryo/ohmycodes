FROM node:22-alpine

WORKDIR /app
RUN npm i -g pnpm@9
COPY package*.json pnpm-lock.yaml ./
RUN pnpm install --frozen-lockfile

COPY . .
RUN pnpm build

EXPOSE 3000

CMD ["node", "build/index.js"]
