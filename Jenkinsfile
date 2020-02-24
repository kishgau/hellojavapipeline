pipeline {
    agent any

    environment {
    JAVA_HOME = '/usr/lib/jvm/java-8-openjdk-amd64/'
}
    stages {
        stage('Build') {
            steps {
                  sh '$JAVA_HOME/bin/java -version'
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
