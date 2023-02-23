pipeline {
    agent any

    
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t bjgomes/flaskapp .'
            }
        }
        stage('Login and Push'){
            steps {
                script{
                    withDockerRegistry(credentialsId: 'Docker') {
                        docker.build('bjgomes/flaskapp').push('latest')
                    }
                }
            }
        }
    }
}


