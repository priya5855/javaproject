def pom
pipeline {
  agent any
  stages {
    stage ('checkout source code') {
      steps {
        // get source code from git repository
        git branch: 'masters', changelog: false, poll: false, url: 'https://github.com/priya5855/Javaproject.git'
          }
    }
    stage ('Build') {
      steps {
        //run the following Maven commands.
        sh '''export PATH=$PATH:/opt/maven/bin
        mvn -Dmaven.test.failure.ignore=true clean package'''
        script {
    // script {
    pom = readMavenPom file: 'pom.xml'
    sh "echo $pom"
              }
            }
      }
    }
  }

              
    
          

