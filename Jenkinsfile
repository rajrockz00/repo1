pipeline {
    agent any

    stages {
        stage('Validate Manifest') {
            steps {
                yamlLint file: '/demo.yaml'
            }
        }
    }
}
