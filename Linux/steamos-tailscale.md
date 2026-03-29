Install:

```bash
$ git clone https://github.com/tailscale-dev/deck-tailscale.git ~/.tailscale
$ sudo -i
$ cd ~deck/.tailscale
$ bash tailsale.sh
$ source /etc/profile.d/tailscale.sh
$ tailscale up --qr --operator=deck --ssh
```

Update every now and then:

```bash
$ cd ~/.tailscale
$ git pull
$ sudo bash tailscale.sh
```