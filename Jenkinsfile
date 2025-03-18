pipeline {
    agent any
    
    stages {
        stage('Checkout Code') {
            steps {
                script {
                    git 'https://github.com/Vinothraja2405/private_repo.git' // Public repo, no credentials needed
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    def myImage = docker.build("hello-python")
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.image("hello-python").run()
                }
            }
        }
    }
}
