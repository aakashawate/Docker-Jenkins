pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'git clone https://github.com/aakashawate/Docker-Jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t Docker-jenkins-app .'
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    sh 'docker run -d -p 3000:3000 --name Docker-jenkins-app Docker-jenkins-app'
                }
            }
        }
    }
}
