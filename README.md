1. Download latest Spark for current Hadoop. Decompress them to home director. 

cd ~/Downloads
tar zxvf spark-2.3.1-bin-hadoop2.7.tgz 
mv spark-2.3.1-bin-hadoop2.6 ~/


2. Setup SPARK_HOME and PATH variables in ~/.bashrc

vim ~/.bashrc
---------------------------------
# .bashrc
...

export SPARK_HOME=/home/cloudera/spark-2.3.1-bin-hadoop2.7
export PATH=$SPARK_HOME/bin:$PATH
export PYSPARK_PYTHON=python3
export PYSPARK_DRIVER_PYTHON=ipython3

3. source ~/.bashrc for the settings to take effect

source ~/.bashrc


4. Test it

[cloudera@quickstart ~]$ which spark-submit
~/spark-2.3.1-bin-hadoop2.7/bin/spark-submit

5. Start the spark cluster

cd ~/spark-2.3.1-bin-hadoop2.7/sbin
./start-all.sh

check 
http://localhost:8080

to see if the master and a worker are running
