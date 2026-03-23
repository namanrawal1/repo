pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main', url: 'git@github.com:namanrawal1/cicd.git'
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
