pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t lekhasricharyan28/cartservice:v1 src/.'
            }
        }
        stage('push'){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh 'docker push lekhasricharyan28/cartservice:v1'
                    }
                }
            }
        }
    }
}
