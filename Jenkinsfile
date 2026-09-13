pipeline {
    agent {
        label 'slave1'
    }

    stages {

        stage('Build') {
            steps {
                bat 'gcc hello.c -o hello.exe'
            }
        }

        stage('Run') {
            steps {
                bat 'hello.exe'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t hello:latest .'
            }
        }

        stage('Run Docker Image') {
            steps {
                bat 'docker run --rm hello:latest'
            }
        }
    }
}