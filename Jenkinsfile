pipeline {
    agent any // Or specify a label or none based on your requirements

    stages {
        stage('Stage 1 Compile') {
            steps {
                // Use the Maven Docker image to build the project
                container('maven:3.9.3') {
                    sh 'mvn clean compile'
                }
            }
        }
        
        stage('Stage 2 test') {
            steps {
                // Use the Maven Docker image to run the tests
                container('maven:3.9.3') {
                    sh 'mvn test'
                }
            }
        }
    }
}
