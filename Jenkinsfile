pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main/newfile.cpp -o myoutput'
                build 'PES1UG21CS813-1'
            }
        }
        stage('Test') {
            steps {
                sh './myoutput'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployed'
            }
        }
    }
    post {
        failure{
            echo 'pipeline failed'
        }
    }
}
