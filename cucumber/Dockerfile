FROM selenium/standalone-chrome:4

USER root
RUN apt-get update && apt-get install -y ruby ruby-dev rubygems libffi-dev \
    clang gcc g++ make mariadb-client libmariadb-dev zip python3-pip \
    apt-transport-https ca-certificates curl software-properties-common \
    && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - \
    && add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" \
    && apt-get install -y docker-ce \
    && curl -L https://github.com/docker/compose/releases/download/1.21.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose \
    && gem install bundler --no-document \
    && pip3 install awscli

USER seluser
