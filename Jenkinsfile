pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                echo "Deploying Portfolio Website..."
                bat """
                    xcopy * "C:\\Program Files\\Apache Software Foundation\\Tomcat 10.1\\webapps\\portfolio\\" /E /Y
                """
            }
        }
    }
}
