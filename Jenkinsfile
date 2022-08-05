pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
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
                sh "chmod +x ./script/*"
                sh 'echo "testing back end"'
                sh './script/backtest.sh'
            }
        }
        stage('Deploy'){
            agent { label 'agent1'}
            steps {
                sh 'echo ------------------DEPLOY---------------------'
                sh 'docker-compose up -d'
            }

        }
        /*stage('Ansible Playbook run'){
            steps{
                sh "ansible-playbook -i ansible-config/inventory.yaml ansible-config/playbook1.yaml"
            
            }
        } */
    }
}