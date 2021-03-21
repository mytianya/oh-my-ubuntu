# ubuntu-install-oracle-jdk8

```shell
sudo mkdir /usr/local/jvm 
sudo tar -zxvf jdk-8u281-linux-x64.tar.gz -C /usr/local/jvm
vim /etc/profile
export JAVA_HOME=/usr/local/jvm/jdk1.8.0_281/
export JRE_HOME=$JAVA_HOME/jre
export CLASSPATH=.:$JAVA_HOME/lib:$JRE_HOME/lib
export PATH=$JAVA_HOME/bin:$PATH
source /etc/profile
java -version
```

