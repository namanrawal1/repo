pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'git@github.com:namanrawal1/cicd.git'
            }

        }
        stage('Build') {
            steps {
                echo 'Building Application...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing application..'
            }
        }
    }
}
