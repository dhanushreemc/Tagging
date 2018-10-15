pipeline {
    agent {label "build"}
    environment {
        def VERSION= sh returnstdout: true, scrip:'sh script.sh'
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
