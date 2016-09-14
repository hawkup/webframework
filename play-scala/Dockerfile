FROM hawkup/scala:2.11.7

RUN apt-get update
RUN apt-get install -y unzip

# Install Activator
RUN \
  wget https://downloads.typesafe.com/typesafe-activator/1.3.7/typesafe-activator-1.3.7.zip && \
  unzip typesafe-activator-1.3.7.zip -d /usr/local/share/

ENV ACTIVATOR_HOME /usr/local/share/activator-dist-1.3.7
ENV PATH $PATH:$ACTIVATOR_HOME 

CMD ["bash"]