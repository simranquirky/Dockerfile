FROM centos:latest
MAINTAINER simran <simrankumari1344@gamil.com>
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
RUN yum install unzip -y
# ncurses allows you to run 'clear' command
RUN yum install ncurses -y
RUN unzip awscliv2.zip
RUN ./aws/install
RUN rm -rf ./aws/ && \ 
    rm -rf awscliv2.zip 
