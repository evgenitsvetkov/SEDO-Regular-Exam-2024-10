pipeline{
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Restore dependencies'){
            steps{
                bat 'dotnet restore'
            }
        stage('Build project'){
            steps{
                bat 'dotnet build'
            }
        }
        stage('Execute tests') {
            steps {
                bat 'dotnet test'
            }
        }
    }
}
