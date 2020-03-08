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
	   stage('SonarQube analysis') {
	      steps {
	        script {
	          // requires SonarQube Scanner 2.8+
	          scannerHome = tool 'SonarQube Scanner 4.2'
	        }
	        withSonarQubeEnv('SonarQube Server') {
	          sh "${scannerHome}/bin/sonar-scanner"
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
        post {
          always {
           cleanWs()
         }
       }


}
