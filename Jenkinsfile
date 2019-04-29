pipeline {
  agent {
    kubernetes {
      label 'maven'
    }

  }
  stages {
    stage('Buzz Build') {
      steps {
        sh 'sleep 10'
        sh './jenkins/build.sh'
      }
    }
    stage('Buzz Test') {
      steps {
        sh './jenkins/test-all.sh'
      }
    }
  }
}