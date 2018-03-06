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
	stage ('git clone') {
	  steps {
	    sh 'ssh rd6-admin@10.251.40.11 cd /tmp/jks_rey/'
		sh 'ssh rd6-admin@10.251.40.11 git clone ssh://git@gitlab.rd6.vir888.com:10022/rd6/playbook.git'
		}
	}
  }
}
