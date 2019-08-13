# Getting a bare Cent OS image
FROM centos

# Setting maintainer 
LABEL maintainer="arghya.gniit@gmail.com"

# Install network tools
RUN yum update; yum install -y net-tools

# Install open jdk & jre 8
RUN  yum install -y java-1.8.0-openjdk java-1.8.0-openjdk-devel

# Install apache web server
RUN  yum install -y httpd

# Copy a simple web page inside  the container
COPY index.html /var/www/html/

# Start apache damon when container runs
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]

# Expose port 80
EXPOSE 80



