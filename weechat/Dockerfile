From debian:jessie

RUN apt-get update && apt-get install -y \
  ca-certificates \
  curl \
  wget \
  libencode-locale-perl

RUN touch /etc/apt/sources.list.d/weechat.list
RUN echo "deb http://debian.weechat.org jessie main" | tee /etc/apt/sources.list.d/weechat.list
RUN apt-get update && apt-get install -y --force-yes weechat-devel

ENV HOME /home/user
RUN useradd --create-home --home-dir $HOME user \
  && mkdir -p $HOME/.weechat \
  && chown -R user:user $HOME

ENV LANG C.UTF-8

WORKDIR $HOME
VOLUME $HOME/.weechat

USER user
CMD ["weechat"]
