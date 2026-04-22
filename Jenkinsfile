pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'python f1.py'
            }
        }
        stage('Test') {
            steps {
                bat 'python f2.py'
            }
        }
        stage('Deploy') {
            steps {
                bat 'python f3.py'
            }
        }
    }
}
