pipeline {
    agent any 
    stages {
        stage('Stage 1 Compile') {
            steps {
                withMaven(maven : 'Mvn'){
					mvn clean compile
				}
            }
        }
        
         stage('Stage 2 test') {
            steps {
                 withMaven(maven : 'Mvn'){
					mvn test
				}
            }
        }

    }
}