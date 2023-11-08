# Use the official Nginx image as the base image
FROM nginx:latest

# Copy the softy-pinko-front-end files to the Nginx web server directory
COPY softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the Nginx configuration file to the correct location
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose the port on which Nginx will listen (recommendation: port 9000)
EXPOSE 9000

# Start Nginx when the container runs
CMD ["nginx", "-g", "daemon off;"]