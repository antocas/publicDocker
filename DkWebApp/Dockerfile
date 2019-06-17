#Descargar Debian
FROM debian

#Actualizarmos APT
RUN apt-get update
RUN apt-get install -y curl python3 python3-dev python3-pip

#Preparamos al sistema para NodeJS
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -

#Actualizamos de nuevo e instalamos de NodeJS
RUN apt-get update
RUN apt-get install -y nodejs

#Actualizamos NMP
RUN npm install -g npm@latest
RUN npm cache clean --force
RUN npm set audit false
RUN npm install -g @angular/cli@latest

#Preparamos flask
RUN pip3 install requests
RUN pip3 install certifi
RUN pip3 install flask
RUN pip3 install flask-cors
RUN pip3 install elasticsearch

#Preparamos entorno
RUN mkdir /home/app
WORKDIR /home/app

CMD /bin/bash
