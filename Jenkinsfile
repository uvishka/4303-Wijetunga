pipeline {
    agent any
    
    stages {
      
        
        stage('Dockerize the application') {
            steps {
                sh "echo '9900' | sudo -S sudo docker build -t frontend ."
            }
        }
        
        stage('Containerize the application') {
            steps {
                sh "echo 'password' | sudo -S  sudo docker run -d -p 5173:5173 frontend"
            }
        }
    }
}
