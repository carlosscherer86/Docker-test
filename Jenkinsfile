pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                step('Create image'){
                    bat "docker build WebApplication13 -t dockertest:${env.BUILD_ID} -f WebApplication13/Dockerfile"
                }

                step('Run image'){
                    bat "docker run -d -p 8081:80 dockertest:lastest"
                }
            }
        }
    }
}