pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning Repository'
            }
        }

        stage('Build Frontend') {
            steps {
                script {
                    bat 'docker build -t docker-frontend ./frontend'
                }
            }
        }

        stage('Build Backend') {
            steps {
                script {
                    bat 'docker build -t docker-backend ./backend'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {

                    bat '''
                    docker rm -f frontend-container 2>NUL
                    docker rm -f backend-container 2>NUL
                    '''

                    bat '''
                    docker run -d --name frontend-container -p 3000:3000 docker-frontend
                    '''

                    bat '''
                    docker run -d --name backend-container -p 5000:5000 docker-backend
                    '''
                }
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful'
        }

        failure {
            echo 'Deployment Failed'
        }
    }
}