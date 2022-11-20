pipeline {
  agent any
  stages {
    stage("verify tooling") {
      steps {
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
        sh 'service docker start'
        sh 'docker compose up -d'
        sh 'docker compose ps'
      }
    }
  }
}
