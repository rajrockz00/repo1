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
    stage("Quality Gate") {
      steps {
        timeout(time: 2, unit: 'MINUTES') {
          waitForQualityGate abortPipeline: true
        }
      }
    }
  }
}
