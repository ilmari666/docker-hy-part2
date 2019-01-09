FROM ubuntu:16.04
EXPOSE 5000
WORKDIR /frontend
RUN apt-get update
RUN apt install -y curl
RUN apt install -y unzip
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN npm install -g serve
RUN curl -L https://github.com/docker-hy/frontend-example-docker/archive/master.zip --output tmp.zip
RUN unzip tmp.zip
RUN rm tmp.zip
RUN cd "frontend-example-docker-master" && npm install && npm run build
#CMD /bin/bash -c 'sleep 3 && serve -s -l 5000 frontend-example-docker-master/dist'
CMD /bin/bash -c 'cd frontend-example-docker-master && npm start'