pipeline {
    agent any

    stages {
        //stage('Clone Repository') {
    //steps {
        // Clone the repository containing the manifest file
        //git credentialsId: 'github', url: 'https://github.com/rajrockz00/repo.git'
    //}
//}
        stage('Validate Manifests') {
            steps {
                git credentialsId: 'github', url: 'https://github.com/rajrockz00/repo.git'
                sh 'kubeval *.yaml'
            }
        }
        
        // Add more stages as needed
    }
    
    // Add post section for post-build actions if required
}
