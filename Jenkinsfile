pipeline {
    agent any
    
     stage('Construir imagen') {
            steps {
                script {
                    def imageName = 'app-php-sergio'
                    def imageTag = 'latest'
                    def dockerfile = 'docker/Dockerfile'
                    
                    // Construir la imagen de Docker
                    docker.build("${imageName}:${imageTag}", "-f ${dockerfile} .")
                }
            }
        }
}
