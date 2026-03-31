# Install Maven on Amazon Linux 2023

### Update the YUM repository
```bash
sudo yum update -y
```

### Install Java as a pre-Requisite 

```bash
sudo yum install java-21-amazon-corretto
```

### Verify Java Version
```bash
java -version
```

### Install Maven
```bash
sudo yum install maven -y
```

### Verif the Maven Version

```bash
mvn -version
```

### Install Git to get the Source code from GitHub

```bash
yum install git -y
```
