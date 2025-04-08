pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }

        stage ('Run App') {
            steps {
                bat 'start "" /b cmd /c "npm start"'
                bat 'ping -n 6 127.0.0.1 > nul'
            }
        }
    }
}
