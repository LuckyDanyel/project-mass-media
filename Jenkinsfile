pipeline {
  agent any
  stages {
    stage("verify tooling") {
      steps {
        sh 'sudo docker compose down'
        sh 'sudo docker system prune -a -f'
        sh '''
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
