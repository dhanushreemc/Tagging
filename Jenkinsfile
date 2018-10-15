pipeline {
    agent {label "build"}
    environment {
        def VERSION= sh returnStdout: true, script: '$(date +%Y_%m_%d).$BUILD_NUMBER'
    }
    stages {
        stage('checkout') {
           steps {
              checkout scm
           }
        }
        stage('test') {
           steps {
              sh "VERSION= $(date +%Y_%m_%d).$BUILD_NUMBER"
              sh "export ${VERSION}"
           }
        }
        stage('launch') {
           steps {
              echo "${VERSION}"
           }
        }
    }
}
