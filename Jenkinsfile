pipeline {
  agent any
  stages {
    stage('Buzz Build') {
      steps {
        sh 'sleep 180'
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