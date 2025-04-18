# Hello Java Maven – Jenkins CI Build

## 🚀 Objective

This project demonstrates a basic **Java HelloWorld** application built using **Maven** in a **Jenkins Freestyle Job**. It's a simple introduction to Continuous Integration (CI) pipelines.

---

## 🧰 Tools Used

- Java JDK 8 (Amazon Linux default)
- Apache Maven
- Jenkins (Docker)
- Amazon Linux EC2
- Git (optional)

---

## 🏗️ Project Structure

hello-java-maven/ ├── pom.xml └── src └── main  └── resources └── java └── HelloApplication.java

---
## 🔧 Setup on EC2 (Amazon Linux)
   
### 1. Install Java, Git
```bashy
um install java-17* git -y
```
### 2. Install Maven
```bash
cd /mnt
mkdir build-tool servers
https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.tar.gz
ls -ltra
tar -xvzf apache-maven-3.9.9-bin.tar.gz
ls -ltra
cd apache-maven-3.9.9-bin.tar.gz
rm -rf apache-maven-3.9.9-bin.tar.gz
cd apache-maven-3.9.9
ls -ltra
pwd
vi .bash_profile
sudo su -
ls -ltra
mvn
unzip apache-tomcat-9.0.104.zip
ls -ltra
rm -rf apache-tomcat-9.0.104.zip
cd apache-tomcat-9.0.104
ls -ltra
```
### 2. Install Jenkins
```bash
cd /mnt
cd webapps
wget https://get.jenkins.io/war-stable/2.452.3/jenkins.war
ls -ltra
chmod -R 777 .
chmod -R 777 ../bin
apache-tomcat-9.0.104]# ls -ltra
./bin/startup.sh
cat /root/.jenkins/secrets/initialAdminPassword
```
### 3.Prepare Project Directory
```bash
ls -ltra
cd /mnt
mkdir hello-java-maven
cd hello-java-maven
```
### 4.Create Java File
```bash
mkdir -p src/main/java
nano src/main/java/HelloWorld.java
```
### 5.Create pom.xml
```bash
nano pom.xml
cat pom.xml
```
```bash
\cat src/main/java/HelloWorld.java
cd /root/.jenkins/workspace/job
ls -ltra
cd /mnt
ls -ltra
[root@ip-172-31-82-154 mnt]# cd hello-java-maven
git init
git status
git config --global user.name pradnyathite91
git config --global user.email pradnyathite91@gmail.com
git remote add origin https://github.com/pradnyathite91/Task8.git
git add .
git commit -m "simple java application"
git push origin master
cd /root/.jenkins/workspace
ls -ltra
pwd
/root/.jenkins/workspace/job/Task8
cd /root/.jenkins/workspace/job/Task8/target
ls -ltra
cd hello-app.jar
cd ..
ls -ltra
java -jar target/hello-app.jar
```

