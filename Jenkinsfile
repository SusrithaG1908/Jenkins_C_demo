pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'gcc hello.c -o hello'
            }
        }

        stage('Run') {
            steps {
                sh './hello'
            }
        }
    }
}pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'gcc hello.c -o hello'
            }
        }

        stage('Run') {
            steps {
                sh './hello'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello:latest .'
            }
        }
    }
}