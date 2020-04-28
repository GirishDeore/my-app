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
        stage ('run') {
            steps {
            

                 
                 sh ' java -jar target/*.jar'
        
            }
        }
        }
    }
