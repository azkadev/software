# Bot Telegram

```dockerfile
FROM ubuntu

WORKDIR /app/

ADD * /app/

RUN apt-get update

RUN apt-get install -y \
    sudo \
    wget \
    neofetch 

RUN wget https://github.com/azkadev/bot_telegram/releases/download/linux-latest/tg-bot-linux.deb
RUN sudo dpkg --force-all -i ./tg-bot-linux.deb

CMD ["tg-bot"]

```


```dockerfile
FROM ubuntu

WORKDIR /app/

ADD * /app/

RUN apt-get update

RUN apt-get install -y \
    sudo \
    wget \
    neofetch 

RUN wget https://github.com/azkadev/bot_telegram/releases/download/linux-latest/tg-bot-linux.deb
RUN sudo dpkg --force-all -i ./tg-bot-linux.deb

CMD ["tg-bot"]

```


```dockerfile
FROM ubuntu

WORKDIR /app/

ADD * /app/

RUN apt-get update

RUN apt-get install -y \
    sudo \
    wget \
    neofetch 

RUN wget --quiet --show-progress http://nz2.archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2.16_amd64.deb
RUN sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2.16_amd64.deb

RUN wget https://github.com/azkadev/userbot/releases/download/latest-linux/userbot-linux.deb
RUN sudo dpkg -i userbot-linux.deb

CMD ["userbot"]
```