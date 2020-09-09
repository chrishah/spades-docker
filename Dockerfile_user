FROM chrishah/ubuntu-basic:18

MAINTAINER <christoph.hahn@uni-graz.at>

WORKDIR /usr/src
#RUN wget ftp://ftp.broadinstitute.org/pub/crd/DiscovarDeNovo/latest_source_code/discovardenovo-52488.tar.gz && \
#	tar xfz discovardenovo-52488.tar.gz 

#SPAdes 3.14.0
RUN wget http://cab.spbu.ru/files/release3.14.0/SPAdes-3.14.0-Linux.tar.gz && \
	tar xfz SPAdes-3.14.0-Linux.tar.gz
	

ENV PATH="${PATH}:/usr/src/SPAdes-3.14.0-Linux/bin"

#add user (not really necessary)
RUN adduser --disabled-password --gecos '' spades
USER spades

WORKDIR /home/spades

