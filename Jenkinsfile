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
    stage ('create file path') {
      steps {
        sh 'ssh rd6-admin@10.251.40.11 mkdir -p /tmp/jks_rey/'
      }
    }
    stage ('git clone') {
      steps {
	sh 'ssh rd6-admin@10.251.40.11 cd /home/rd6-admin/playbook/; git pull; cp /home/rd6-admin/playbook/compose/qa/docker-compose-up.yml /tmp/jks_rey/docker-compose-up.yml'
	sh 'ssh rd6-admin@10.251.40.11 cat /tmp/jks_rey/docker-compose-up.yml'
      }
    }
  }
}
