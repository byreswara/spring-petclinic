pipeline {
    agent any
      tools {
       maven 'maven'
           }
    stages {
        stage('sonar-analasys') {
            steps {
               withCredentials([file(credentialsId: '', variable: 'sonar_cred')]) {
                withSonarQubeEnv('sonar') {
                 sh 'mvn sonar:sonar -Dsonar.projectKey=petclinick -Dsonar.login=$sonar_cred -Dsonar.host.url=http://13.212.177.149:9000/'
		               // sh 'sonar-scanner -Dsonar.projectKey=myproject -Dsonar.sources=src'
                }
              }    
            }
        }
    }
}
