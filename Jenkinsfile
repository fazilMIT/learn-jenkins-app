pipeline {
    agent any

    stages {
        stage('without docker') {
            steps {
                echo 'Hello World'
            }
        }
        stage('with docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                sh 'echo "with docker"'
                sh 'npm --version'
            }
        }
    }
}
