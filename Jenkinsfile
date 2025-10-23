pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t lekhasricharyan28/paymentservice:v1 .'
            }
        }
        stage('push'){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh 'docker push lekhasricharyan28/paymentservice:v1'
                    }
                }
            }
        }
    }
}
