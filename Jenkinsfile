pipeline {
    agent {label "build"}
    stages {
        stage('checkout') {
           steps {
              checkout scm
           }
        }
        stage('setting env') {
           steps {
               sh "export VERSION= $(date +%Y_%m_%d).$BUILD_NUMBER"
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
