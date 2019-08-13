---
layout: post
title:  "PySpark Setup on Mac"
date:   2019-08-12 18:23:10 +0530
categories: posts
---

## 1. Install Java 8 or higher
* Check if Java 8 or higher is installed: Open terminal and type `java -version`. If Java is installed, then no error message should be returned. 
* If not installed, go to https://www.oracle.com/technetwork/java/javase/downloads/index.html, download and install JDK. 

## 2. Down Spark
Go to http://spark.apache.org/downloads.html and download the latest version of Spark. Unzip it, and move it to `/opt/`: 
```bash
sudo mv spark-2.4.3-bin-hadoop2.7 /opt/
```

## 3. Add Spark to path
Add the path of Spark so your bash knows where to find it. If `~/.bash_profile` or `~/.bashrc` exists, add the following into the file (whichever exists):
```bash
export SPARK_HOME=/opt/spark-2.4.3-bin-hadoop2.7/
export PATH=$SPARK_HOME/bin:$PATH
```

## 4. Test whether the setup is successful
Restart the terminal, and type `pyspark`, this should return: 
```
Welcome to
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /__ / .__/\_,_/_/ /_/\_\   version 2.4.3
      /_/

Using Python version 3.6.8 (default, Dec 29 2018 19:04:46)
SparkSession available as 'spark'.
>>> 
```

## 5. (optional) PySpark setup in Jupyter notebook
* Install `findspark`: `pip install findspark`
* Launch jupyter notebook (One way from the terminal is typing `Jupyter notebook`)
* Firstly, import `findspark` and initiate it:
  ```python
  import findspark
  findspark.init()
  ```
* Now we can import `PySpark` and start using it:
  ```python
  import pyspark
  ```


