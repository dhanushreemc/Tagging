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
              sh "script.sh"
              sh "export VERSION"
          
        }
        stage('launch') {
           steps {
              echo "${VERSION}"
           }
        }
    }
}
