# # Use the official Node.js image.
# FROM node:18-alpine

# # Set the working directory
# WORKDIR /app

# # Copy the dependency files
# COPY package.json package-lock.json ./

# # Install dependencies
# RUN npm install

# # Copy the application files
# COPY . .

# # Build the React application
# RUN npm run build

# # Install a simple HTTP server to serve the static files
# RUN npm install -g serve

# # Start the React application
# CMD ["serve", "-s", "build"]


FROM node:alpine
# Set the working directory
WORKDIR /app
# Copy the package.json and package-lock.json files
COPY package*.json ./
# Install the dependencies
RUN npm install
# Copy the app files
COPY . .
# Build the app
RUN npm run build
# Expose the port
EXPOSE 3000
# Run the app
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0" ]