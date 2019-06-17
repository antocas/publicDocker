FROM openjdk:8u181-jre-stretch


RUN apt-get update
RUN apt-get install --no-install-recommends -y wget unzip

RUN wget http://nlp.stanford.edu/software/stanford-corenlp-full-2018-10-05.zip


RUN unzip stanford-corenlp-full-2018-10-05.zip
RUN mv stanford-corenlp-full-2018-10-05 /corenlp

WORKDIR /corenlp

RUN wget http://nlp.stanford.edu/software/stanford-spanish-corenlp-2018-10-05-models.jar
RUN export CLASSPATH="stanford-spanish-corenlp-2018-10-05-models.jar"


EXPOSE 9000

CMD java -mx4g -cp "*" edu.stanford.nlp.pipeline.StanfordCoreNLPServer -serverProperties StanfordCoreNLP-spanish.properties -port 9000 -timeout 3600000
