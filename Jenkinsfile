pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
               sh "ant dist"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy"
            }
        }
    }
}
