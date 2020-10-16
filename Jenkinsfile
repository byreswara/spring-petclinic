pipeline {
    agent any
      tools {
       maven 'maven'
           }
    stages {
        stage('sonar-analasys') {
            steps {
               
                withSonarQubeEnv('sonar') {
                 sh 'mvn sonar:sonar -Dsonar.host.url=http://13.229.63.99:9000  -Dsonar.login=cafa036d60191e4726ca1c2266648a9fbb2f99c7 -Dsonar.analysis.mode='
		               // sh 'sonar-scanner -Dsonar.projectKey=myproject -Dsonar.sources=src'
                }
                 
            }
        }
    }
}
