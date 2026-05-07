pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Je récupère le code depuis GitHub...'
                checkout scm
            }
        }

        stage('Vérification') {
            steps {
                echo 'Je vérifie que le fichier index.html existe...'
                bat 'dir'
            }
        }

        stage('Déploiement') {
            steps {
                echo 'Je déploie le site web...'
                bat 'echo Site déployé avec succès !'
            }
        }

    }

    post {
        success {
            echo '✅ Pipeline terminé avec succès !'
        }
        failure {
            echo '❌ Une erreur est survenue !'
        }
    }
}
