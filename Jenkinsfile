pipeline {
    agent any
    stages {
        stage ('git checkout') {
            steps {
               git credentialsId: 'github',url: 'https://github.com/GirishDeore/my-app.git'
            }
        }
         stage ('Build') {
            steps {
              sh "mvn --version"
              sh "mvn clean install"
            }
        }
        }
    }
