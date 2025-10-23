pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t lekhasricharyan28/loadgenerator:v1 .'
            }
        }
        stage('push'){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh 'docker push lekhasricharyan28/loadgenerator:v1'
                    }
                }
            }
        }
    }
}
