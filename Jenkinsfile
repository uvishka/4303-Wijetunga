pipeline {
    agent any
    
    stages {
      
        
        stage('Dockerize the application') {
            steps {
                sh ' docker build -t frontend .'
            }
        }
        
        stage('Containerize the application') {
            steps {
                sh ' docker run -d -p 5173:5173 fsrontend'
            }
        }
    }
}
