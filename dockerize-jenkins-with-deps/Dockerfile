FROM jenkins/jenkins:lts

USER root
RUN apt update

# Default available
# Curl 

# Install Python3 
RUN apt install software-properties-common -y
# RUN add-apt-repository ppa:deadsnakes/ppa -y 
RUN apt update
RUN apt install python3 -y

# Install pip 
RUN apt install python3-pip -y

# Install php7
RUN apt install -y curl wget gnupg2 ca-certificates lsb-release apt-transport-https
RUN wget https://packages.sury.org/php/apt.gpg
RUN apt-key add apt.gpg
RUN echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | tee /etc/apt/sources.list.d/php7.list
RUN apt update
RUN apt install -y php7.4 php7.4-cli php7.4-common

# Install eyeD3 (python)
RUN pip3 install eyed3

# Install atomicparsley
RUN apt install atomicparsley -y

# Install ffmpeg
RUN apt install ffmpeg -y

# Install ImageMagick
RUN apt install build-essential -y
RUN wget https://www.imagemagick.org/download/ImageMagick.tar.gz
RUN tar xvzf ImageMagick.tar.gz
RUN rm -rf ImageMagick.tar.gz
RUN cd $(ls | grep ImageMagick) && ./configure && make && make install && ldconfig /usr/local/lib

# Check Installed
RUN curl --version
RUN python3 --version 
RUN php --version
RUN pip3 list | grep eyed3
RUN AtomicParsley --version
RUN ffmpeg -version
RUN magick -version

# Fall back to jenkins user
USER jenkins