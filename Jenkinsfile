stage('Validate Manifest') {
    steps {
        script {
            def manifestFile = '/demo.yaml'
            def schemaFile = '/demo.yaml'

            // Validate the manifest against the schema
            validate file: manifestFile, schema: schemaFile
        }
    }
}
