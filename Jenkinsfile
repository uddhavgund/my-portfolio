pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                    npm install
                '''
            }
        }

        stage('Deploy to EC2') {
            steps {
                sh '''
                    sudo rm -rf /var/www/html/*
                    sudo cp -r * /var/www/html/
                '''
            }
        }
    }
}
