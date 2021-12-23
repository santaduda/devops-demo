pipeline {
    agent any
    stages {
        stage('Quality check') {
          steps {
                echo "Quality passed"
                sh "ls -l"
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
