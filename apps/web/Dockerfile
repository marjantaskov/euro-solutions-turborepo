# apps/web/Dockerfile
FROM node:20-alpine

WORKDIR /app
RUN npm install -g pnpm@8.7.6

COPY . .
RUN pnpm install -r --frozen-lockfile --filter=web...

CMD ["pnpm", "--filter", "web", "run", "dev"]
