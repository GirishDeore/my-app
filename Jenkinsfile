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
                 sh 'scp -o StrictHostKeyChecking=no target/*.txt ec2-user@13.233.229.40'
        }
            }
        }
        }
    }
