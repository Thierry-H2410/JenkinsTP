/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'node:22.2.0-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
}
