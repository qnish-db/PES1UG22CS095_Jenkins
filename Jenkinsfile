pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o my_program my_specific_file.cpp' 
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './my_program' 
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
