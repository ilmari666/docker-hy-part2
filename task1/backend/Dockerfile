FROM ubuntu:16.04
EXPOSE 8000
WORKDIR /backend
RUN apt-get update
RUN apt install -y curl
RUN apt install -y unzip
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN curl -L https://github.com/docker-hy/backend-example-docker/archive/master.zip --output tmp.zip
RUN unzip tmp.zip
RUN rm tmp.zip
RUN mv backend-example-docker-master/* ./
RUN npm install
CMD /bin/bash -c 'npm start'