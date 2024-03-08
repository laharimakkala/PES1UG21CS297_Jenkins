pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                build job: 'PES1UG21CS291-1', wait: false
                echo 'Build by CS291 successful'
            }
        }
        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                echo 'Test by CS291 successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy by CS291 successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
