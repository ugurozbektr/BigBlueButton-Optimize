#Temel görüntü debian'ı indirin
FROM  node

# Uygulama dizini oluşturun
WORKDIR /root
# Özel görüntü hakkında ETİKET
LABEL maintainer="iletisim@dogangokce.com"
LABEL version="0.1"
LABEL description="Bu, için özel Docker Görüntüsüdür"

#Yazılım Deposunu Güncelle
RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app
#RUN apt-get -y curl
RUN curl -sS -o - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add
RUN echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" > /etc/apt/sources.list.d/google-chrome.list
RUN apt-get -y update
RUN apt-get -y install google-chrome-stable
RUN apt-get -y install software-properties-common
RUN add-apt-repository ppa:jonathonf/ffmpeg-4
#RUN apt-get -y update
RUN apt-get -y install ffmpeg
RUN apt -y install xvfb
RUN git clone https://github.com/manishkatyan/bbb-mp4
RUN cd bbb-mp4 && npm install --ignore-scripts
WORKDIR /root/BigblueButon-Optimize/kayit
