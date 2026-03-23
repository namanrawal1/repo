pipeline {
    agent any
    environment {
    PATH = "/opt/homebrew/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"
    }
     stages{
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-nginx-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker rm -f nginx-container || true
                docker run -d -p 9090:80 --name nginx-container my-nginx-app
                '''
            }
        }
    }
}
