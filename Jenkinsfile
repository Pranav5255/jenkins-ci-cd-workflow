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
                bat 'timeout /t 5'
            }
        }
    }
}
