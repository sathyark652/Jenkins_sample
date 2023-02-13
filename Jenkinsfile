pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ PES2UG20CS315.cpp -o PES2UG20CS315'
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG20CS315'
            }
        }
        stage('Deploy') {
            steps {
                // deploy steps here
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
