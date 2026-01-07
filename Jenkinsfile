pipeline {
    agent any
    stages {
        stage('Connection Test') {
            steps {
                echo '------------------------------------'
                echo 'Hello Jenkins! Network is working!!!'
                echo '------------------------------------'
            }
        }
        stage('Check Environment') {
            steps {
                sh 'curl -I https://github.com'
            }
        }
    }
}
