pipeline {
    agent {
        node {
            label 'devops1-mikail'
        }
    }

    stages {
        stage('Build Apps') {
            steps {
                echo 'Build Apps'
            }
        }

        stage('Testing Apps') {
            steps {
                echo 'Testing Apps'
            }
        }

        stage('Scanning Code') {
            steps {
                echo 'Scanning Code'
            }
        }

        stage('Dockerized') {
            steps {
                echo 'Dockerized'
            }
        }

        stage('Push Image') {
            steps {
                echo 'Push Image'
            }
        }

        stage('Deploy to Docker') {
            steps {
                echo 'Deploy to Docker'
            }
        }
    }
}
