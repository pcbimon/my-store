FROM nginx:stable-alpine

# Copy the nginx configuration file
COPY ./nginx.conf /etc/nginx/nginx.conf
# COPY SSL certificate and key
COPY ./ssl/nginx-selfsigned.crt /etc/nginx/ssl/nginx-selfsigned.crt
COPY ./ssl/nginx-selfsigned.key /etc/nginx/ssl/nginx-selfsigned.key

# Expose port 80 and 443
EXPOSE 80 443

# Start nginx
CMD ["nginx", "-g", "daemon off;"]