pipeline {
   agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
        
      }
    }
    stage('sonar') {
    environment {
        scannerHome = tool 'SonarQubeScanner'
    }
    steps {
        withSonarQubeEnv('sonarqube') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
        timeout(time: 10, unit: 'MINUTES') {
            //waitForQualityGate abortPipeline: true
        }
    }
}
  }
}
