
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t Lekhasricharyan28/adservice:v1 .'
            }
        }
        stage('push'){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'newdocker-cred') {
                        sh 'docker push Lekhasricharyan28/adservice:v1'
   
                    }
                }
                
            }
        }
    }    
}
