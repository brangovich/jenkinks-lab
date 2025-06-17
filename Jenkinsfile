pipeline {
    agent any

    stages {
        stage('Clonar proyecto') {
            steps {
                git 'https://github.com/brangovich/jenkins-lab.git'
            }
        }

        stage('Instalar dependencias') {
            steps {
                sh 'pip install -r mlops/requirements.txt'
            }
        }

        stage('Entrenar modelo') {
            steps {
                sh 'python3 mlops/train_model.py'
            }
        }

        stage('Desplegar API') {
            steps {
                sh 'nohup uvicorn mlops.api:app --host 0.0.0.0 --port 8000 &'
            }
        }
    }
}
