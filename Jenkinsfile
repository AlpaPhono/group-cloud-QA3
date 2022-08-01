pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker-compose build --parallel && docker-compose up -d && docker-compose push'
            }
        }
        /*stage('Test') {
            steps {
                //
            }
        }
        stage('Deploy') {
            steps {
                //
            }
        } */
    }
}