pipeline {
    agent any
    stages {
        stage('SonarQube analysis') {
            def scannerHome = tool 'SonarScanner 4.0';
            withSonarQubeEnv('My SonarQube Server') {
              sh "${scannerHome}/bin/sonar-scanner"
            }
        }
        stage('Build') {
            steps {
                echo "Build completed"    
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy completed"    
            }
        }
    }
}
