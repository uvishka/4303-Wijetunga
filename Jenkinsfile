pipeline {
    agent any
    
    stages {
      
        
        stage('Dockerize the application') {
            steps {
                sh 'sudo docker build -t frontend . -S'
            }
        }
        
        stage('Containerize the application') {
            steps {
                sh 'sudo docker run -d -p 5173:5173 frontend'
            }
        }
    }
}
