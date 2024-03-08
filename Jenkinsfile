pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ new.cpp -o new'
                build job: 'PES1UG21CS297-1', wait: false
                echo 'Build by CS297 successful'
            }
        }
        stage('Test') {
            steps {
                sh 'cat new.cpp'
                echo 'Test by CS297 successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy by CS297 successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
