pipeline {
    agent any
    
    stages {
        stage('Get from SCM') {
            steps {
                git 'https://github.com/uvishka/4303-Wijetunga'
            }
        }
        
        stage('Dockerize the application') {
            steps {
                sh 'sudo docker build -t frontend .'
            }
        }
        
        stage('Containerize the application') {
            steps {
                sh 'sudo docker run -d -p 5173:5173 fsrontend'
            }
        }
    }
}
