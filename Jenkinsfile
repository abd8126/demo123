pipeline {
    agent {
        label 'jenkins-agent'
    }
    stages {
        stage('Build and Push') {
            steps {
                script {
                    def image = docker.build("caching_${BUILD_NUMBER}", "-f Dockerfile .")
                    image.push("caching_${BUILD_NUMBER}")
                }
            }
        }
    }
}
