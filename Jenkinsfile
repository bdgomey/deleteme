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
                echo 'dckr_pat_5VARXbC8wv4wzaAAGUoXJThN6Co | docker login --username bjgomes --password-stdin'
            }
        }    
    }
}



// dckr_pat_5VARXbC8wv4wzaAAGUoXJThN6Co