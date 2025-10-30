# Use minimal basse image
FROM nginx:alpine

# Set nginx working directory 
WORKDIR /usr/share/nginx/html

# Copy the application into the ngnix working directory
COPY index.html .

# Overide ngnix default configuration
COPY nginx.conf  /etc/nginx/conf.d/default.conf

# Expose the container
EXPOSE 8080

# Health check to verify the web server is running
HEALTHCHECK --start-period=5s --interval=10s --timeout=5s --retries=3 \
  CMD wget -q --spider http://127.0.0.1:8080 || exit 1

# Start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]