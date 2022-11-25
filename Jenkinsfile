pipeline {
  agent any
  stages {
    stage("pulling stage") {
      steps {
        sh 'sudo docker pull elasticsearch:8.5.1'
      }
    }
    stage("delete images stage") {
      steps {
        sh 'sudo docker system prune -a -f'
      }
    }
    stage("build images for container") {
      steps {
        sh 'sudo docker compose build'
      }
    }
    stage("down containers") {
      steps {
        sh 'sudo docker compose down'
      }
    }
    stage('Start containers') {
      steps {
        sh 'sudo docker compose up -d'
      }
    }
  }
}
