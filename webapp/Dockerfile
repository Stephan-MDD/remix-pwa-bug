FROM node:20-alpine
WORKDIR /webapp

COPY package.json .
COPY package-lock.json .

COPY . .

RUN npm ci

CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]