pipeline {
    agent any
    environment{
       DOCKER_LOG = credentials('DOCKER_LOG')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo $DOCKER_LOG_USR $DOCKER_LOG_PSW'
                sh 'docker login -u $DOCKER_LOG_USR -p $DOCKER_LOG_PSW'
                sh 'docker-compose build --parallel && docker-compose up -d && docker-compose push'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "testing back end"'
                sh 'cd spring-petclinic-rest'
                sh 'sudo apt install maven -y'
                sh 'mvn test'
            }
        }
       /* stage('Deploy') {
            steps {
                //
            }
        } */
    }
}