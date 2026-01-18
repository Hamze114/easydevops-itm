pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                dir('frontend') {
                    bat '"C:\\Program Files\\dotnet\\dotnet.exe" build frontend.csproj --configuration Release'
                }
            }
        }

        stage('Test') {
            steps {
                dir('frontend') {
                    bat '"C:\\Program Files\\dotnet\\dotnet.exe" test'
                }
            }
        }
    }
}
