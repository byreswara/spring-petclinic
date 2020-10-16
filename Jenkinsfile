pipeline {
    agent any
      tools {
       maven 'maven'
           }
    stages {
        stage('sonar-analasys') {
            steps {
               
                withSonarQubeEnv('sonar') {
                 sh 'mvn sonar:sonar'
		               // sh 'sonar-scanner -Dsonar.projectKey=myproject -Dsonar.sources=src'
                }
              }    
            }
        }
    }
}
