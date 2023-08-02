pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/sardaralii/webAppforJenkins.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        // Add more stages as needed (e.g., deployment, integration tests, etc.)
    }

    post {
        always {
            // Clean up and perform any post-build tasks
        }

        success {
            // Actions to perform when the build and tests are successful
        }

        failure {
            // Actions to perform when the build or tests fail
        }
    }
}
