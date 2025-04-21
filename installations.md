#Install Java, maven On Ubuntu
sudo apt update -y
apt install openjdk-17-jdk -y
# If any issuws wrt brken
apt --fix-broken install
cd /opt/
#wget https://dlcdn.apache.org/maven/maven-3/3.8.7/binaries/apache-maven-3.8.7-bin.tar.gz
wget https://dlcdn.apache.org/maven/maven-3/3.8.8/binaries/apache-maven-3.8.8-bin.tar.gz
tar -xzvf apache-maven-3.8.8-bin.tar.gz
export PATH=$PATH:/opt/apache-maven-3.8.8/bin
mvn --version


# To make mvn avaialble after we exit also, do the following steps : for sudo only 
vi /etc/profile.d/maven.sh
export PATH=$PATH:/opt/apache-maven-3.8.7/bin
export M2_HOME=/opt/apache-maven-3.8.7
sudo chmod +x /etc/profile.d/maven.sh
source /etc/profile.d/maven.sh
