pipeline {
    agent any

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
