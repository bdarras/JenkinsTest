pipeline {
    agent any

 
    stages {
        stage('Checkout') {
            steps {
                scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo "helloWorld!"'
            }
        }
    }
}