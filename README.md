# Install-Java-and-Jenkins-in-EC2
Install Jenkins from scratch on an ec2 instance with default plugins

- Prerequisites:

A machine with, 256 MB of RAM, although more than 2 GB is recommended

10 GB of drive space (for Jenkins and your Docker image)

The following software installed:

Java 17 or 21

Docker (navigate to Get Docker site to access the Docker download that’s suitable for your platform)

- Launch an EC2 instance, Use Amazon Linux 2 and connect.
- Allow inbound ports: 22 (SSH), 8080 (Jenkins).
- Change to root user using command (sudo su -) optional
- Enter below commands to import official jenkins setup and install jenkins.
  
  **sudo wget -O /etc/yum.repos.d/jenkins.repo \ https://pkg.jenkins.io/redhat-stable/jenkins.repo**

  **sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key**

  **sudo yum install –y jenkins**

  OR    

  **sudo yum install Jenkins -y**

- Install Java version 17 or 21 with below commands:

  **sudo yum install -y java-17-amazon-corretto**
  OR
  **sudo yum install -y java-21-amazon-corretto**

- Check or update the Java version use below commands:

  **java -version**
  
  **update-alternatives --config java**

- Update software in EC2 instance, to enable, start, status of jenkins use below commands.

  **sudo yum upgrade**
  
  **systemctl enable jenkins**
  
  **systemctl start jenkins**
  
  **systemctl status jenkins**
  
  **systemctl restart jenkins (optional)**

- Copy the public ip of the ec2 server and browse as : http://publicip:8080

- Copy the path from the jenkins page and paste in EC2 terminal , **/var/lib/jenkins/secrets/initialAdminPassword**
- Get the password and paste in jenkins to unlock it.
- Enter username and password and email to create jenkins account and login.
- You can start putting Jenkins to work!





