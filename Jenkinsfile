pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'dotnet restore WebApplication13/WebApplication13.csproj'
            }
        }
    }
}