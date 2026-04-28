FROM mcr.microsoft.com/devcontainers/universal:5-linux

RUN apt-get update && \
    python3 -m pip install --upgrade pip && \
    python3 -m pip install django
      FROM node:20-alpine

// To install Express
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy project
COPY . .

# Build Next.js (optional for prod)
RUN npm run build

EXPOSE 3000

CMD ["npm", "run", "dev"]
