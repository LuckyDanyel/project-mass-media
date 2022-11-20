pipeline {
  agent any
  stages {
    stage("verify tooling") {
      steps {
        sh 'service docker start'
        sh '''
          docker version
          docker info
          sudo docker compose version 
        '''
      }
    }
    stage('Start container') {
      steps {
        sh 'sudo docker compose up -d'
        sh 'sudo docker compose ps'
        sh 'sudo docker compose --follow'
      }
    }
  }
}
