pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
              ant {
                 target('clean')
                 target('dist')
                 buildFile('build.xml')
                 javaOpt('-Xmx1g')
                 antInstallation('Ant 1.8')
              }
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
