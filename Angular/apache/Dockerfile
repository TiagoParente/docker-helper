# Base image
FROM nginx:latest

# Remove default nginx website
RUN rm -rf /usr/share/nginx/html/*

# Copy the build files from local machine to container
COPY dist/html /usr/share/nginx/html

# Expose port 80 to the host
EXPOSE 80
