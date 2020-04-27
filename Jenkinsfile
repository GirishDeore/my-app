pipeline {
    agent any
    stages {
        stage ('git checkout') {
            steps {
               git credentialsId: 'github',url: 'https://github.com/GirishDeore/my-app.git'
            }
        }
         stage ('maven build') {
            steps {
              tool name: '/etc/profile.d/maven.sh', type: 'maven'
            }
        }
        }
    }
