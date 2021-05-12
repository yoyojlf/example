pipeline {
  agent {
    docker {
      image 'node:12'
      args '--network jenkins-blue-ocean-tutorial_jenkins-net'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'cd ./example-react; npm install'
      }
    }

  }
}