FROM hang/builder-maven:2.1.4

RUN curl https://download.java.net/java/GA/jdk9/9.0.4/binaries/openjdk-9.0.4_linux-x64_bin.tar.gz | tar -xz
RUN mv /home/jenkins/jdk-9.0.4 /usr/java
RUN rm /usr/bin/java /usr/bin/javac
RUN ln -s /usr/java/bin/java /usr/bin/java
RUN ln -s /usr/java/bin/javac /usr/bin/javac
ENV JAVA_HOME /usr/java

CMD ["mvn","-version"]
