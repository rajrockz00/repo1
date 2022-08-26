pipeline {
   agent any
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv('h2db') { 
         sh'mvn sonar:sonar'
        }
      }
    }
    
  }
}
