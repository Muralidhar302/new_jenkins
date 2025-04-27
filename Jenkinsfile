pipeline{
    agent any
    stages {
        stage('CHECKOUT') {
            steps {
                script {
                    echo "This is a checkout stage"
                }
            }                
        }
        stage('BUILD') {
            steps {
                echo "This is a buliding code stage"
                sh '''
                pwd
                hostnamectl
                '''
            }
        }
        stage('TEST1') {
            steps {
                script { 
                    echo "This is a testing  stage"
                }
                sh '''
                uname -a
                whoami
                '''
            }
        }
        stage('TEST2') {
            steps {
                echo "This is a testing  stage2"
                sh '''
                uptime
                date
                '''
            }
        }
        stage('QA') {
            steps {
                script {
                    echo "This is a checking stage"
                }
            }
        }
        stage('DEPLOY') {
            steps {
                script {
                    echo "This is a depolying stage"
                }
            }
        }

    }
}