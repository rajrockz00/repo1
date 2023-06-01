pipeline {
    agent any

    stages {
        stage('Validate Manifests') {
            steps {
                sh 'kubeval demo.yaml'
            }
        }
        
        // Add more stages as needed
    }
    
    // Add post section for post-build actions if required
}
