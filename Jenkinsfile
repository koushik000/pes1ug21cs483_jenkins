pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'pes1ug21cs483'
                sh 'g++ main/newfile.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
