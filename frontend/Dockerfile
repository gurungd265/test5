# Use official Node.js image
FROM node:18-alpine AS builder

# Set working directory
WORKDIR /app

# Copy only package.json and lock file first
COPY package*.json ./

# Install dependencies inside container
RUN npm install

# Copy rest of the code
COPY . .

# Build the app
RUN npm run build

# Serve with Nginx or any other way in next stage...
