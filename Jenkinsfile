pipeline {
  agent {
    docker {
      image 'node:12'
      args '--network jenkins-server_docker-net'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'cd ./example; npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'cd ./example-react; npm run test -- --coverage --watchAll=false'
      }
    }

  }
}