pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage ('Run App') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}