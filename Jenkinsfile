pipeline {
    agent {label "build"}
    environment {
        def VERSION= sh returnstdout: true, scrip:'$(date +%Y_%m_%d).$BUILD_NUMBER'
    }
    stages {
        stage('checkout') {
           steps {
              echo "${VERSION}"
           }
        }
        stage('test') {
           steps {
              echo "${VERSION}"
           }
        }
        stage('launch') {
           steps {
              echo "${VERSION}"
           }
        }
    }
}
