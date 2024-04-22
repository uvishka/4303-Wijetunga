pipeline {
    agent any
    
    stages {
      
        
        stage('Dockerize the application') {
            steps {
                sh "echo '9900' | sudo -S  docker build -t frontend ."
            }
        }
        
        stage('Containerize the application') {
            steps {
                sh "echo 'password' | sudo -S  docker run -d -p 5173:5173 frontend"
            }
        }
    }
}
