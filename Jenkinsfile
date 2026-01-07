pipeline {
    agent any
    
    // [추가된 부분] 파이프라인 전체에 적용될 환경변수 설정
    environment {
        http_proxy = 'http://192.168.111.100:3128'
        https_proxy = 'http://192.168.111.100:3128'
        no_proxy = 'localhost,127.0.0.1,192.168.0.0/16,10.96.0.0/12'
    }

    stages {
        stage('Connection Test') {
            steps {
                echo '------------------------------------'
                echo 'Hello Jenkins! Network is working! Success'
                echo '------------------------------------'
            }
        }
        stage('Check Environment') {
            steps {
                // 프록시 환경변수가 잘 들어갔는지 확인하고 요청
                sh 'printenv | grep proxy'
                sh 'curl -I https://github.com'
            }
        }
    }
}