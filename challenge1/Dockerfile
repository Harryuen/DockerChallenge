# Use the official Nginx image from the Docker Hub
FROM nginx:alpine

# Copy the content of the public folder to the Nginx html directory
COPY public /usr/share/nginx/html

# Expose port 8080
EXPOSE 8080

# Start Nginx server
CMD ["nginx", "-g", "daemon off;"]