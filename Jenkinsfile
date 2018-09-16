pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat "docker build WebApplication13 -t dockertest:${env.BUILD_ID} -f WebApplication13/Dockerfile.dev ."
            }
        }
    }
}