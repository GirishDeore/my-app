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
        stage ('Deploy') {
            steps {
                
                 sh 'scp -o StrictHostKeyChecking=no target/*.jar ec2-user@13.233.229.40'
        
            }
        }
        }
    }
