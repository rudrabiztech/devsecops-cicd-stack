FROM jenkins/jenkins:lts-jdk11
USER root
RUN apt update -y ; apt install apt-transport-https ca-certificates curl gnupg -y
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker.gpg
RUN echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker.gpg] https://download.docker.com/linux/debian bookworm stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
RUN apt update -y ; apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin -y
USER jenkins
