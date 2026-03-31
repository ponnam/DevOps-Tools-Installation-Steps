# Jenkins Installation on Amazon Linux 2023

### Pre-Requisites

Jav21
Port number 8080 must be opened to access the Jenkins UI

### Update YUM Repository

```bash
sudo yum update -y
```

### Install Java21+ as a dependency

```bash
sudo yum install java-21-amazon-corretto -y

```
### Verify the Java Version

```bash
java -version
```

## Jenkins Installation Steps

### Add the Jenkins Repository
```bash
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/rpm/jenkins.repo
```

### Update the YUM repository with Jenkins related

```bash
sudo yum upgrade -y
```

### Install Git & Maven as we are building JAVA application and source code repo is GitHub

```bash
sudo yum install git -y
sudo yum install maven -y
```

### Install Jenkins

```bash
sudo yum install Jenkins -y
```

### Check the Jebkins service Status, Then Start the Jenkins Server and configure to auto start.

```bash
sudo systemctl status jenkins
sudo systemctl start jenkins
sudo systemctl daemon-reload
sudo chkconfig jenkins on
```

### Get the Initial password to login to Jenkins portal

```bash
cat /var/lib/jenkins/secrets/initialAdminPassword
```

### Access the Jenkins Portal and login by entering the above password.

http://IPADDRESS:8080


### Complete the Initial setup of Jenkins

- Follow on-screen instructions to
    - Create a user account to login to Jenkins
    - Install all default plugins

