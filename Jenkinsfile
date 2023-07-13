pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                dotnetBuild configuration: 'Release'
            }
        }
        stage('Pack') {
            steps {
                script {
                    dotnetPack
                 }
            }
        }
        stage('Deploy') {
            steps {
                 script {
                     dotnetNuGetPush
                 }
            }
        }
    }
}