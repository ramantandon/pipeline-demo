pipeline {
  agent {
    kubernetes {
      label 'mymaven'
    }

  }
  stages {
    stage('Buzz Build') {
      steps {
        sh 'sleep 10'
        sh './jenkins/build.sh'
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true)
      }
    }
    stage('Buzz Test') {
      steps {
        sh './jenkins/test-all.sh'
      }
    }
  }
}