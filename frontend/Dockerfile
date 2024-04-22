# Use the official Node.js image as a base
FROM node:alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the entire React app to the working directory
COPY . .

# Build the React app for production
RUN npm run build
EXPOSE 5173

# Command to run the React app
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
