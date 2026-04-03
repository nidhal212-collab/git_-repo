pipeline {
    agent any

    stages {

        stage('display message') {
            steps {
                echo 'Hello, this is a Jenkins pipeline for Java application!'
            }
        }

        stage('Checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/nidhal212-collab/git_-repo.git'
            }
        }

        stage('Compile code') {
            steps {
                sh 'mkdir -p bin'
                sh 'javac -d bin src/application/Test.java'
            }
        }

        stage('Execute code') {
            steps {
                sh 'java -cp bin application.Test'
            }
        }
    }
}