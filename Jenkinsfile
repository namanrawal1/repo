pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/<your-username>/jenkins-demo.git'
            }
        }

        stage('System Info') {
            steps {
                sh 'whoami'
                sh 'pwd'
                sh 'ls -lrt'
            }
        }
    }
}
