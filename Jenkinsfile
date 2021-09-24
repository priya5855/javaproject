#!groovy
@Library('my-shared-library@master')

pipeline {
 agent any
stages {
stage ('checkout scm') {
steps {
 	//get source code from git repository
	}
}
stage ('Build') {
steps {
	//run the following maven command
sh "export PATH=$PATH:/home/ec2-user/maven"
sh "source /etc/profile"
sh "mvn Dmaven.test.failure.ignore=true clean package"
}
}
}
}

