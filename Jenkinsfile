pipeline {
    agent any
    environment{
        DOCKER = credentials('Docker')
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t bjgomes/flaskapp .'
            }
        }
        stage('Push image') {
            steps{
                echo '$DOCKER | docker login --username bjgomes --password-stdin'
            }
        }    
    }
}



// dckr_pat_5VARXbC8wv4wzaAAGUoXJThN6Co