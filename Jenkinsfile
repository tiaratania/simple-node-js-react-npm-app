pipeline {
    agent { //specifing agent
        docker{
        image 'node:lts-buster-slim'
        args '-u root:root'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}
