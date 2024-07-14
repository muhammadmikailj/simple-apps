pipeline {
    agent {
        node {
            label 'devops1-mikail'
        }
    }

    stages {
        stage('Build Apps') {
            steps {
                sh '''
                cd app
                npm install
                '''
            }
        }

        stage('Testing Apps') {
            steps {
                sh'''
                cd app
                npm test
                npm run test:coverage
                '''
            }
        }

        stage('Scanning Code') {
            steps {
                sh'''
                cd app
                 sonar-scanner   -Dsonar.projectKey=Simple-Apps   -Dsonar.sources=.   -Dsonar.host.url=http://172.23.10.11:9000   -Dsonar.login=sqp_343c49b96bcf0a973c18a8434f01998c8fc975a2
                '''
            }
        }

        stage('Dockerized') {
            steps {
                sh '''
                docker compose build
                '''
            }
        }

        stage('Push Image') {
            steps {
                sh '''
                docker compose push
                '''
            }
        }

        stage('Deploy to Docker') {
            steps {
                echo 'Deploy to Docker'
            }
        }
    }
}
