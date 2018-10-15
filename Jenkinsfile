pipeline {
    agent {label "build"}
    environment {
         VERSION= """${sh(
                returnStdout: true,
                script: '$(date +%Y_%m_%d).$BUILD_NUMBER'
            )}"""
         
    }
    stages {
        stage('checkout') {
           steps {
              checkout scm
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
