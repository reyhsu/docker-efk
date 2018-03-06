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
      }
    }
    stage ('create file path) {
      steps {
        sh 'ssh rd6-admin@10.251.40.11 mkdir -p /tmp/jks_rey/'
      }
    }
	stage('docker  cp') {
      steps {
        sh 'ssh rd6-admin@10.251.40.11 docker cp rey_jenkins:/tmp/docker-compose.yml /tmp/docker-compose.yml'
		sh 'cat /tmp/docker-compose.yml'
      }
    }
  }
}
