pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script{
                dotnetBuild configuration: 'Release'
                dotnetPack configuration: 'Release'
                dotnetNuGetPush
                }
            }
        }
    }
}