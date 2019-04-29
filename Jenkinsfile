pipeline {
  agent {
    docker {
      image 'docker.io/ramantandon/jnlp-slave_with_mvn:0.1'
      args '${computer.jnlpmac} ${computer.name}'
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