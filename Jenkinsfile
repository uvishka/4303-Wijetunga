pipeline {
    agent any
    
    stages {
        stage('Get from SCM') {
            steps {
                dir('frontend') {
                    git 'https://github.com/uvishka/4303-Wijetunga'
                }
            }
        }
        
        stage('Dockerize the application') {
            steps {
                dir('frontend') {
                    sh 'sudo docker build -t frontend .'
                }
            }
        }
        
        stage('Containerize the application') {
            steps {
                dir('frontend') {
                    sh 'sudo docker run -d -p 5173:5173 frontend'
                }
            }
        }
    }
}