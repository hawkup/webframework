FROM hawkup/java:8

RUN apt-get update
RUN apt-get install -y unzip
RUN apt-get install -y curl

# Install SDKMAN(The Software Development Kit Manager)
RUN curl -s get.sdkman.io | bash

# Install Grails
RUN /bin/bash -c "source $HOME/.sdkman/bin/sdkman-init.sh && sdk install grails"

CMD ["bash"]