sudo apt update
sudo apt install openjdk-8-jdk -y

java -version

wget https://downloads.apache.org/pig/latest/pig-0.17.0.tar.gz

tar -xvzf pig-0.17.0.tar.gz

sudo mv pig-0.17.0 /opt/pig

nano ~/.bashrc

export PIG_HOME=/opt/pig
export PATH=$PIG_HOME/bin:$PATH
export PIG_CLASSPATH=$HADOOP_HOME/conf

source ~/.bashrc

pig -version

$HADOOP_HOME/sbin/start-dfs.sh
$HADOOP_HOME/sbin/start-yarn.sh

pig -x mapreduce

quit;
