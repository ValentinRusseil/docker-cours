FROM node:22-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install
COPY . .

# Pour le build en production et CI/CD
# RUN npm ci --omit=dev --no-audit --not-fund && npm run build && npm cache clean --force
RUN npm run build

EXPOSE 8080
CMD ["npm", "run", "preview"]