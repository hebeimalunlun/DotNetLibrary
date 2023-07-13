pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                dotnetBuild configuration: 'Release'
                dotnetPack
                dotnetNuGetPush
            }
        }
    }
}