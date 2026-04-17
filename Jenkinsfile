pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Pratiksha-2004-gif/devops-cicd-project.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t my-app .'
            }
        }

        stage('Run App') {
            steps {
                sh 'docker run -d -p 8081:8080 my-app'
            }
        }
    }
}
