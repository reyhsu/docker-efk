pipeline {
  agent any
  stages {
    stage('steg1') {
      parallel {
        stage('steg1') {
          steps {
            sh 'cat docker-compose.yml;cp docker-compose.yml /tmp/'
          }
        }
        stage('steg2') {
          steps {
            sh 'ls -al'
          }
        }
      }
    }
  }
}