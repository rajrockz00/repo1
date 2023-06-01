pipeline {
    agent any

    stages {
        stage('Validate Manifests') {
            steps {
                kubeval {
                    files '**/*.yaml'
                }
            }
        }
        
        // Add more stages as needed
    }
    
    // Add post section for post-build actions if required
}
