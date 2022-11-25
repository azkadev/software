# Software

Semua software yang ada disini berbayar tidak ada yang gratis


<p align="center">
    <a href="https://github.com/azkadev">
        <img src="https://telegra.ph/file/e90bdeab8390b8c0d9df2.png" alt="Specta"
            width="312"
            height="312">
    </a>
    <br>
    <a href="https://youtube.com/c/galaxeus">
        <img
            src="https://raw.githubusercontent.com/azkadev/azkadev/main/assets/images/powered_galaxeus.png"
            alt="galaxeus"
            width="350"
            height="80"
        >
    </a>
    <br>
    <b>Author Azkadev 🔥</b>
    <br>
</p>
 

### Support
> Tolong beri saya dukungan dengan cara follow up semua social media saya / donate di github ya

### Social Media Me

1. [Youtube](https://youtube.com/@azkadev)
2. [Telegram](https://t.me/azkadev)

---

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