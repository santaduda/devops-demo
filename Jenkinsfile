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
        stage("Quality Gate"){
                timeout(time: 1, unit: 'HOURS') {
                    def qg = waitForQualityGate(abortPipeline: true)
                    if (qg.status != 'OK') {
                        error "Pipeline aborted due to quality gate failure: ${qg.status}"
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
