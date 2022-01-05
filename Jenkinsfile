pipeline {
    agent any
    tools {
        maven 'M3'
    }
    stages {
        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv("My SonarQube Server") {
                    sh "mvn clean verify sonar:sonar -Dsonar.projectKey=DevOps-Demo"
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
