# Use official Node.js image
FROM node:18-alpine 

WORKDIR /app

# Copy only package.json and package-lock.json first
COPY src/package*.json ./

# Use npm install with force to fix dependency issues
RUN npm install --production --silent --legacy-peer-deps

# Copy the rest of the project files
COPY . .

# Expose the application port
EXPOSE 3000

# Start the application
CMD ["node", "server.js"]
