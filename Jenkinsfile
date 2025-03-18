pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Vinothraja2405/private_repo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t hello-python .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run hello-python'
                }
            }
        }
    }
}
