pipeline {
    agent any // You can specify a specific agent or label here if needed

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your Git repository
                // Replace 'your-git-repo-url' with the actual URL of your Git repository
                // and 'your-git-credentials-id' with the ID of your Git credentials configured in Jenkins
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
                          userRemoteConfigs: [[url: 'https://github.com/sardaralii/webAppforJenkins.git']],
                          credentialsId: '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'])
            }
        }
        
        stage('Build') {
            steps {
                // Use the Maven Docker image to build the project
                // Replace 'maven:3.9.3' with the appropriate Docker image if needed
                container('maven:3.9.3') {
                    sh 'mvn clean package'
                }
            }
        }
        
        stage('Test') {
            steps {
                // Use the Maven Docker image to run the tests
                container('maven:3.9.3') {
                    sh 'mvn test'
                }
            }
        }
    }
}
