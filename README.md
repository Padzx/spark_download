OBS: Downloading Spark for Linux Machine (Ubuntu)

1 - Download JDK Oracle: [https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.tar.gz](https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.tar.gz) ([sha256](https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.tar.gz.sha256))

Download JDK For Terminal Linux:

```bash
sudo apt-update
sudo apt install openjdk-<version-jdk>-jdk # For Example
sudo apt install openjdk-11-jdk
```

2 - Unzip the jdk file this command `tar -xvf` and move the file `mv`

```bash
sudo mv jdk /opt/jdk
```

3- Configure your variable enviroments:

```bash
#jdk
export JAVA_HOME=/opt/jdk 
export PATH=$PATH:$JAVA_HOME/bin
```

4- Download Spark:  [spark-3.5.0-bin-hadoop3.tgz](https://www.apache.org/dyn/closer.lua/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz)


5- Unzip the spark file this command `tar -xvf` and move the file `mv`

```bash
sudo mv spark-3.1.1-bin-hadoop2.7 /opt/spark
```

6- In directory home configure your variable enviroments with command `gedit .bashrc`

```bash
#Spark
export SPARK_HOME=/opt/spark 
export PATH=$PATH:$SPARK_HOME/bin
```


## Download Anaconda 

1 - Download Anaconda: https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Linux-x86_64.sh

2- Installing Anaconda with this command `bash`

```bash
bash anaconda3-2023.09-0-Linux-x86_64.sh
```

3- Configure your variable enviroments PySpark

```bash
#PySpark
export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH
export PYTHONPATH_DRIVER_PYTHON="jupyter"
export PYSPARK_DRIVER_PYTHON_OPTS="notebook"
export PYSPARK_PYTHON=python3
```

For testing the Pyspark just you make this command: `pyspark` in your terminal, like this it will open an GUI Jupyter Notebook with pyspark

OBS: After the changes in `gedit bashrc` you need save the changes utilizing this command `source .bashrc` for to save the changes whitout need restart your machine Linux.