pipeline {
    agent any
    stages {
        stage('Construir imagen') {
            steps {
                script {


                    def branchName = "${env.BRANCH_NAME}".replaceAll('/', '-')
                    def imageName = '${branchName}-php-${buildNumber}'
                    def imageTag = 'latest'
                    def dockerfile = 'docker/Dockerfile'
                    
                    // Construir la imagen de Docker
                    docker.build("${imageName}:${imageTag}", "-f ${dockerfile} .")

                }
            }
        }
    }
}
