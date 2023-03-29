pipeline {
   agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
        
      }
    }
    stage('sonar') {
      steps {
        withSonarQubeEnv('sonar') {
            sh "ls"
        }
        timeout(time: 10, unit: 'MINUTES') {
            //waitForQualityGate abortPipeline: true
        }
    }
}
  }
}
