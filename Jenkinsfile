pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'gcc main/newfile.cpp -o myoutput'
                build 'PES1UG21CS813-1'
            }
        }
        stage('Test') {
            steps {
                sh 'myoutput.exe'
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
