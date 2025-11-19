pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }

        stage('Deploy') {
            steps {
                timeout(time: 1, unit: 'MINUTES') {
                    retry(3) {
                        sh '''
                            echo "Tentative de déploiement..."
                            # ici on simule un script flakey-deploy.sh
                            # pour l’instant on fait juste un echo
                            echo "Déploiement OK (simulation)"
                        '''
                    }
                }
            }
        }
    }

    post {
        always {
            echo 'Post: ceci s’exécute toujours (cleanup, logs, etc.)'
        }
        success {
            echo 'Post: pipeline terminé avec SUCCÈS'
        }
        failure {
            echo 'Post: pipeline en ÉCHEC'
        }
    }
}
﻿
snop9790
snop9790
 
