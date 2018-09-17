pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat "docker build WebApplication13 -t dockertest:${env.BUILD_ID} -f WebApplication13/Dockerfile"
                bat "docker run -d -p 8081:80 dockertest:lastest"
            }
        }
    }
}