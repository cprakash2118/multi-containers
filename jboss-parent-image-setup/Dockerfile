FROM ubi7/ubi:7.7
MAINTAINER Your Name <youremail>
LABEL description="A custom Apache container based on UBI 7"
RUN yum install -y httpd && \
    yum install -y java && \
    yum install -y unzip && \
 yum clean all
RUN echo "Hello from Dockerfile" > /var/www/html/index.html
RUN useradd jboss && \
    echo "redhat" | passwd --stdin jboss 
EXPOSE 80
CMD ["httpd", "-D", "FOREGROUND"]

