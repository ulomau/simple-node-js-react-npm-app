pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
  }
  
  environment {
    CI = 'true' 1
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') { 2
      steps {
        sh './jenkins/scripts/test.sh' 3
      }
    }
  }
}
