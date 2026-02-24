# Use official PHP image
FROM devopsedu/webapp

# Copy your PHP website files to container
COPY . /var/www/html/

# Expose HTTP port
EXPOSE 8080
# Start Apache server

CMD ["/bin/bash", "-c", "/usr/sbin/apache2ctl -D FOREGROUND"]
