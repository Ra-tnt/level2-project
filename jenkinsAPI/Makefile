#you can create the access token in jenkins
#press on the user id "admin" > configure > API token > press "add new token" > press "generate" > copy the token and paste it here instead of the token word

#dont forget to install "github integration plugin" before using the files


all:
	project department office person role

project:
	java -jar jenkins-cli.jar -s http://15.185.210.44/jenkins/ -auth admin:token create-job project-assessment-site < project-assessment-site.xml

department:
	java -jar jenkins-cli.jar -s http://15.185.210.44/jenkins/ -auth admin:token create-job department-service < department-service.xml

office:
	java -jar jenkins-cli.jar -s http://15.185.210.44/jenkins/ -auth admin:token create-job office-service < office-service.xml

person:
	java -jar jenkins-cli.jar -s http://15.185.210.44/jenkins/ -auth admin:token create-job person-service < person-service.xml

role:
	java -jar jenkins-cli.jar -s http://15.185.210.44/jenkins/ -auth admin:token create-job role-service < role-service.xml



