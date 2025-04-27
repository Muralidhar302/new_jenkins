pipeline{
    environment {
        APP= 'frontend'
        ENV= 'main'
        USER= 'murali'
    }

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
        parallel (Tesing parallel)
        parallel {
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
        }
        
        stage('ENVIRONMENT') {
            steps {
                script {
                    echo "This is a environment checking stage"
                    echo "grovvy-------> APP_TYPE:${env.APP}" 
                }
                echo "grovvy-------> USER_NAME:${env.USER}"
                sh '''
                echo "grovvy-------> TARGET_ENV:${ENV}"
                '''


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