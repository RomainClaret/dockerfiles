# dockerfiles
My "everyday" dockerfiles

## Install docker
https://docs.docker.com/engine/install/ubuntu/

```bash
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

```bash
$ sudo mkdir -m 0755 -p /etc/apt/keyrings
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```bash
$ echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```bash
$ sudo apt update
```

```bash
$ sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

```bash
$ sudo docker run hello-world
```