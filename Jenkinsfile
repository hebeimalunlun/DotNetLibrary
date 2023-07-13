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
                dotnetPack
            }
        }
        stage('Deploy') {
            steps {
                dotnetNuGetPush
            }
        }
    }
}