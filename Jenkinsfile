pipeline {
    agent any
    environment {
    PATH = "/opt/homebrew/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"
    }
    stages {
        stage('Debug') {
    steps {
        sh 'echo $PATH'
        sh 'which docker || true'
            }
        }  

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker stop myapp-container || true
                docker rm myapp-container || true
                docker run -d -p 8000:8000 --name myapp-container myapp
                '''
            }
        }
    }
}
