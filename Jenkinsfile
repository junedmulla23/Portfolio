pipeline {
    agent any

    stages {
        stage('Pull from GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/junedmulla23/Portfolio.git'
            }
        }

        stage('Build & Deploy') {
            steps {
                echo 'Deploying website to Jenkins workspace...'
                bat 'mkdir C:\\inetpub\\wwwroot\\portfolio || echo folder exists'
                bat 'xcopy /s /y * C:\\inetpub\\wwwroot\\portfolio'
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful!'
        }
        failure {
            echo 'Deployment Failed!'
        }
    }
}
