FROM ubuntu:14.04

MAINTAINER https://github.com/hawkup

RUN apt-get update
RUN apt-get install -y software-properties-common

RUN apt-get install -y curl

# Install RVM
RUN \
  gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 && \
  curl -sSL https://get.rvm.io | bash -s stable --rails

RUN echo "source $HOME/.rvm/scripts/rvm" >> $HOME/.bashrc

CMD ["bash"]