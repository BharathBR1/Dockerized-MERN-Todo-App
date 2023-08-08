FROM node:14.16.0-alpine3.13

WORKDIR /app

COPY package*.json ./

RUN --mount=type=cache,target=/app/.npm \
  npm set cache app/.npm && \
  npm install

COPY . .

EXPOSE 3000

CMD ["npm","start"]



