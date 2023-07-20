pipeline {
    agent any
    stages {
        stage('Construir imagen') {
            steps {
                script {
                    def branchName = "${env.BRANCH_NAME}".replaceAll('/', '-')
                    def buildNumber = "${env.BUILD_NUMBER}"
                    def imageName = "${branchName}-build-${buildNumber}"
                    def dockerfilePath = 'docker/Dockerfile'
                    
                    
                    sh "docker build -t ${imageName} -f ${dockerfilePath} ."

                }
            }
        }
    }
}
