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
        stage('ls -al /tmp') {
          steps {
            sh 'ls -al'
          }
        }
      }
    }
    stage('docker  cp') {
      steps {
        sh 'cd /tmp;docker cp rey_jenkins:/tmp/docker-compose.yml .'
      }
    }
    stage (‘Deploy’) {
      steps {
        sh 'ssh root@10.251.40.11 mkdir /tmp/jks_rey/ -R'
  }
}
