pipeline {
    agent any
    stages {
        stage('Construir imagen') {
            steps {
                script {
                    def imageName = 'app-php-sergio'
                    def imageTag = 'latest'
                    def dockerfile = 'docker/Dockerfile'
                    
                    docker.build("${imageName}:${imageTag}", "-f ${dockerfile} .")
                }
            }
        }
    }
}
