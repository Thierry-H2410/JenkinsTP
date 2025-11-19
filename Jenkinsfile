pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'echo Hello World'

                bat '''
                    echo Multiline batch steps works too
                    dir
                '''
            }
        }

        stage('Deploy') {
            steps {
                timeout(time: 1, unit: 'MINUTES') {
                    retry(3) {
                        bat '''
                            echo Tentative de déploiement...
                            echo Deploiement OK (simulation)
                        '''
                    }
                }
            }
        }
    }

    post {
        always {
            echo 'Post: ceci se lance toujours (cleanup, logs, etc.)'
        }
        success {
            echo 'Post: pipeline terminé avec SUCCES'
        }
        failure {
            echo 'Post: pipeline en ECHEC'
        }
    }
}
