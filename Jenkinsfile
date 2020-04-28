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
        stage ('Delpoy') {
            steps {
            

                 sshagent(['tomcat-dev']) {
                 sh 'scp -o StrictHostKeyChecking=no target/*.jar ec2-user@172.31.37.68'
        }
            }
        }
        }
    }
