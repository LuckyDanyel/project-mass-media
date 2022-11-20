pipeline {
  agent any
  stages {
    stage("verify tooling") {
      steps {
        sh 'service docker start'
        sh '''
          docker version
          docker info
          docker compose version 
          curl --version
          jq --version
        '''
      }
    }
    stage('Start container') {
      steps {
        sh 'docker compose up -d'
        sh 'docker compose ps'
      }
    }
  }
}
