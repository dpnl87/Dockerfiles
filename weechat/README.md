# Weechat

> WeeChat is a fast, light and extensible chat client.
> http://www.weechat.org

## Building
```bash
docker build -t dpnl87/weechat .
```
## Starting
```bash
docker run -it \
  -v $HOME/.weechat:/home/user/.weechat \
  --read-only \
  --name weechat \
  dpnl87/weechat
```
