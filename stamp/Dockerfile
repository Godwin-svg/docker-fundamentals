# Set application base image
FROM alpine:3.20 

# Set working directory
WORKDIR /app  

# Install  dependencies
RUN apk add  --no-cache tzdata 

# Set default command to print UTC timestamp
CMD date -u +"%Y-%m-%dT%H:%M:%SZ"