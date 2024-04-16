pipeline {
    agent any

    stages {
        stage('Build & Tag Docker Image') {
            steps {
                withDockerRegistry(credentialsId: 'docker-creds', toolName: 'docker') {
                 sh "docker build -t rajith08/adservice:latest"    
                }
            }
        }
        stage('Push Docker Image') {
            steps {
                withDockerRegistry(credentialsId: 'docker-creds', toolName: 'docker') {
                 sh "docker push -t rajith08/adservice:latest"    
                }
            }
        }
    }
}
