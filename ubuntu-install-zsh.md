# ubuntu-install-zsh

## install zsh
```shell
sudo apt-get install zsh
```

## change current use shell to zsh

```shell
chsh -s /bin/zsh
sudo vim /etc/passwd
#/bin/bash change to /bin/zsh
root:x:0:0:root:/root:/bin/zsh
```

## install oh-my-zsh

```shell
sudo apt install curl
#vim /etc/hosts add
185.199.108.133 raw.githubusercontent.com
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

