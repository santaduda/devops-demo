pipeline {
    agent any
    tools {
        maven 'M3'
    }
    stages {
        stage('SonarQube') {
            steps {
                withSonarQubeEnv("My SonarQube Server") {
                    sh "mvn clean verify sonar:sonar -Dsonar.projectKey=devops-demo -Dsonar.sources=src -Dsonar.language=java -Dsonar.java.binaries=."
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
