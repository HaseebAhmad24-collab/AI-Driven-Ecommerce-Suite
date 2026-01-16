# Use Node.js base image
FROM node:18-slim

# Set working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy project files
COPY . .

# Expose port (Vite default is 5173)
EXPOSE 5173

# Run development server
# Note: --host is needed for Docker to expose the port correctly
CMD ["npm", "run", "dev", "--", "--host"]
