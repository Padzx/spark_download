OBS: Downloading Spark for Linux Machine (Ubuntu)

1 - Download JDK Oracle: [https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.tar.gz](https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.tar.gz) ([sha256](https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.tar.gz.sha256))

Download JDK For Terminal Linux:

```bash
sudo apt-update
sudo apt install openjdk-<version-jdk>-jdk # For Example
sudo apt install openjdk-11-jdk
```

2 - unzip the jdk file this command `tar -xvf` and move the file `mv`

```bash
sudo mv jdk /opt/jdk
```

3- Configure your variable enviroments:

```bash
export JAVA_HOME=/caminho/para/seu/jdk 
export PATH=$PATH:$JAVA_HOME/bin
```

4- Download Spark:  [spark-3.5.0-bin-hadoop3.tgz](https://www.apache.org/dyn/closer.lua/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz)


5- unzip the spark file this command `tar -xvf` and move the file `mv`

```bash
sudo mv spark-3.1.1-bin-hadoop2.7 /opt/spark
```

6- In directory home configure your variable enviroments with command `gedit .bashrc`

```bash
export SPARK_HOME=/caminho/para/seu/spark 
export PATH=$PATH:$SPARK_HOME/bin
```


## Download Anaconda 