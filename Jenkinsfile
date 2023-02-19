pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output new_working_file.cpp'
                build job : 'PES1UG20CS619-1'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './output'
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
            echo 'Pipeline execution failed'
        }
    }
}
