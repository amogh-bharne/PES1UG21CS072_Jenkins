pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS072-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed!'
        }
    }
}
