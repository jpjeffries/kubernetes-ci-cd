FROM nginx:latest

COPY index.html /usr/share/nginx/html/index.html
COPY DockerFileEx.jpg /usr/share/nginx/html/DockerFileEx.jpg

EXPOSE 80

FROM  jenkins/jenkins:lts
USER root
RUN apt-get -qq update  && apt-get -qq -y install --no-install-recommends curl
RUN curl -sSL https://get.docker.com/ | sh
RUN usermod -aG docker jenkins
USER jenkins