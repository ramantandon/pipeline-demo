pipeline {
  agent {
    docker {
      image 'maven'
    }

  }
  stages {
    stage('Buzz Build') {
      steps {
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