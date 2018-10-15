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
               sh "export BUILDTAG=`(date +%Y_%m_%d)`"
               echo "${BUILDTAG}"
           }
        }
        stage('launch') {
           steps {
              echo "${BUILDTAG}"
           }
        }
    }
}
