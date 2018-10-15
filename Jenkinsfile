pipeline {
    agent {label "build"}
    environment {
         VERSION= sh '$(date +%Y_%m_%d).$BUILD_NUMBER'
         
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
