pipeline {
    agent any

 
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo "helloWorld!"'
                sh 'echo BRANCH_NAME'
            }
        }
    }
}