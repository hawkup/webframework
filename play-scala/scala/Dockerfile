FROM hawkup/java:8

# Install Scala
RUN \
  wget www.scala-lang.org/files/archive/scala-2.11.7.deb && \
  dpkg -i scala-2.11.7.deb && \
  apt-get update && \
  apt-get install scala && \
  wget http://dl.bintray.com/sbt/debian/sbt-0.13.9.deb && \
  dpkg -i sbt-0.13.9.deb && \
  apt-get update && \
  apt-get install sbt