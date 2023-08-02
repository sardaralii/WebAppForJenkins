pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Clone the Git repository containing your Java application
                // Replace 'your-repo-url' with the actual URL of your repository
                git 'https://github.com/sardaralii/webAppforJenkins.git'
            }
        }

        stage('Build') {
            steps {
                // Clean and build the Java application using Maven
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Run tests using Maven
                sh 'mvn test'
            }
        }
    }
}
