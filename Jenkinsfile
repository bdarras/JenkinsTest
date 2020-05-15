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
            }
        }

        stage('NON PROD (Not master)') {
            when {
                not {
                    branch 'master'
                }
            }
            steps {
                sh 'echo "Not MASTER"'
            }
        }


        stage('PROD (master)') {
            when {
                branch 'master'
            }
            steps {
                sh 'echo "MASTER"'
            }
        }


        stage('Example') {
            steps {
                script { 
                    if (env.BRANCH_NAME != 'master' && env.BRANCH_NAME != 'staging') {
                        echo 'This is not master or staging'
                    } else {
                        echo 'things and stuff'
                    }
                }
            }
        }
        

    }
}