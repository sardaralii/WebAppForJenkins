pipeline {
    agent any 
    stages {
        stage('Stage 1 Compile') {
            steps {
              sh 'mvn clean compile'

            }
        }
        
         stage('Stage 2 test') {
            steps {
                sh 'mvn test'
		
            }
        }

    }
}