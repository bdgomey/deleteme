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
        stage('Login'){
            steps {
                echo '$DOCKER | docker login -u bjgomes --password-stdin'
            }
        }
        stage('Push'){
            steps {
                sh 'docker push bjgomes/flaskapp'
            }
        }
    }
}


