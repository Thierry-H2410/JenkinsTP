pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Commande Windows (CMD)
                bat 'echo Hello from Jenkins on Windows'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Running simple tests...'
            }
        }
    }
}
