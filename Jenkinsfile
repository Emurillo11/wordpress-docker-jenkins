pipeline {
    agent any

    stages {
        stage('Checkout desde Git') {
            steps {
                checkout scm
            }
        }

        stage('Detener ambiente anterior') {
            steps {
                bat 'docker compose down'
            }
        }

        stage('Desplegar WordPress') {
            steps {
                bat 'docker compose up -d'
            }
        }

        stage('Verificar contenedores') {
            steps {
                bat 'docker ps'
            }
        }
    }

    post {
        success {
            echo 'Despliegue realizado correctamente.'
        }

        failure {
            echo 'El despliegue presentó errores.'
        }
    }
}