pipeline {
    agent any

    stages {
        stage('Build & Tag Docker Image') {
            steps {
                script {
                   withDockerRegistry(credentialsId: 'docker-creds', toolName: 'docker') {
                      sh "docker build -t rajith08/paymentservice:latest ."    
                   }
                }
                
            }
        }
        stage('Push Docker Image') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-creds', toolName: 'docker') {
                       sh "docker push  rajith08/paymentservice:latest"    
                    }
                }
            }
        }
    }
}
