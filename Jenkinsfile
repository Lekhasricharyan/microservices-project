pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t Lekhasricharyan/service:v1 .'
            }
        }
        stage('push'){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'newdocker-cred') {
                        sh 'docker push Lekhasricharyan/service:v1'
   
                    }
                }
                
            }
        }
    }    
}
