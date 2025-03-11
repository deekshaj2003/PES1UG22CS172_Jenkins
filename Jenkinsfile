pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS172-1 nonexistent.cpp' // Intentional error: File does not exist
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS172-1' 
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deploying the application..."
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed' 
        }
    }
}
