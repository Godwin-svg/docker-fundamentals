# Use  minimal base image
FROM alpine:3.20 

# Create a non-root user
RUN adduser -u 1000 -D newuser

# Set working directory
WORKDIR /app

# Give newuser ownership of the working directory
RUN chown -R newuser:newuser /app

# Copy startup script
COPY . .

# Make script executable
RUN chmod +x startup.sh

# Set environment variable
ENV APP_ENV=dev

# Switch to non-root user
USER newuser

# Launch the script
ENTRYPOINT ["./startup.sh"]