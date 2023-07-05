pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker-compose up --build'
            }
        }

        stage('Test') {
            steps {
                sh 'docker-compose up --build'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker-compose down'
                sh 'docker-compose up --build'
            }
        }

        stage('Monitoring') {
            steps {
                sh 'docker-compose -f docker-compose-monitoring.yml up --build'
            }
        }
    }
    
}
