# Hello Java Maven – Jenkins CI Build

## 🚀 Objective

This project demonstrates a basic **Java HelloWorld** application built using **Maven** in a **Jenkins Freestyle Job**. It's a simple introduction to Continuous Integration (CI) pipelines.

---

## 🧰 Tools Used

-Java JDK 8 (Amazon Linux default)
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
### 3.Set Up Jenkins
`Login using the admin password.
Install Suggested Plugins.
Create admin user (or skip and continue).`

### 3.Configure Maven in Jenkins
- Go to: Manage Jenkins → Global Tool Configuration
- Scroll to Maven, click Add Maven
- Name: Maven 3.9.9`

### 4.Prepare Project Directory
```bash
ls -ltra
cd /mnt
mkdir hello-java-maven
cd hello-java-maven
```
### 5.Create Java File
```bash
mkdir -p src/main/java
nano src/main/java/HelloWorld.java
```
### 6.Create pom.xml
```bash
nano pom.xml
cat pom.xml
```
### 7.Create Jenkins Freestyle Job

1.Open Jenkins: http://<EC2-IP>:8080
2.Click New Item → Enter name java-maven-build → Select Freestyle project
3.Under Source Code Management:
- If using GitHub: https://github.com/pradnyathite91/Task8.git
- If building local: skip
4.Under Build section:
- Click Add build step → Invoke top-level Maven targets
5.Set Goals: -f Task8/pom.xml clean install
-Click Save
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

