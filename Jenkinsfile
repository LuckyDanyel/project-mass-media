pipeline {
  agent any
  stages {
    stage("verify tooling") {
      steps {
        sh 'docker compose down'
        sh 'sudo docker system prune -a'
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
      }
    }
  }
}
