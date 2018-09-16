pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat "docker build WebApplication13/Dockerfile.prod -t dockertest:${env.BUILD_ID}"
            }
        }
    }
}