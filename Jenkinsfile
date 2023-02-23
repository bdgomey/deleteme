pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t bjgomes/flaskapp .'
            }
        }
        stage('Push image') {
            steps{
                script{
                    withDockerRegistry([ credentialsId: "dockerhubaccount", url: "" ]) {
                    dockerImage.push()
                    }
                }
            }

        }    
    }
}



dckr_pat_5VARXbC8wv4wzaAAGUoXJThN6Co