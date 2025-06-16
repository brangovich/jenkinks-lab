pipeline {
    agent any
    stages {
        stage('Saludo') {
            steps {
                echo '👋 ¡Hola desde Jenkins!'
            }
        }
        stage('Listar archivos') {
            steps {
                sh 'ls -la'
            }
        }
    }
}
