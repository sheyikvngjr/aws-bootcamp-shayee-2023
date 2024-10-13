# Use an official Node.js runtime as a parent image
FROM node:16.18

# Set the working directory
WORKDIR /frontend-react-js

# Copy package.json and package-lock.json separately for better caching
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Set the PORT environment variable
ENV PORT=3000

# Expose the port the app runs on
EXPOSE ${PORT}

# Start the application
CMD ["npm", "start", "--", "--host", "0.0.0.0"]
 