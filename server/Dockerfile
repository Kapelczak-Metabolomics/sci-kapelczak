FROM node:20-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./

# Use npm install instead of npm ci
RUN npm install

# Copy rest of the server files
COPY . .

# Build (if using TypeScript or bundler)
RUN npm run build

EXPOSE 5000

CMD ["node", "dist/index.js"]
