pipeline {
    agent  { docker { image 'maven:3.9.3' } }
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
