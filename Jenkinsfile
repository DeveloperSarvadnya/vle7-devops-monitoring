pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t vle7-myapp:latest .'
            }
        }

        stage('Verify Image') {
            steps {
                sh 'docker image inspect vle7-myapp:latest'
            }
        }
    }
}
