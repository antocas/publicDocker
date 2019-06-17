from ubuntu

RUN apt-get update
RUN apt-get install -y cron build-essential python3.7 python3.7-dev python3.7-distutils nano


RUN mkdir /scripts
WORKDIR /scripts

RUN service cron start

ENTRYPOINT ["/scripts/entrypoint.sh"]

CMD /bin/bash
