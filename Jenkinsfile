pipeline {
    agent any
    stages {
        stage('SonarQube Analysis') {
            steps {
                def mvn = tool 'Default Maven';
                withSonarQubeEnv("My SonarQube Server") {
                    sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=DevOps-Demo"
                }
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
