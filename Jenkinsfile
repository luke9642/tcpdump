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
        sh 'env'
        sh 'apk add libc-dev gcc openssl-dev make libpcap-dev git'
        sh './configure'
      }
    }
  }
}