pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'apk add sudo'
                sh 'sudo chown -R $(whoami) ~/.npm'
                sh 'npm install' 
            }
        }
    }
}