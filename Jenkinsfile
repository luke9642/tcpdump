pipeline {
  agent any
  stages {
    stage('Build') {
      agent {
        docker {
          image 'alpine'
        }

      }
      steps {
        sh './configure'
        sh '''apt update
apt install libc-dev gcc openssl-dev make libpcap-dev git'''
      }
    }
  }
}