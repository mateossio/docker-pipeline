pipeline {
  agent any
  stages {
    stage('Echo test') {
      steps {
        sh 'echo "Hello World"'
      }
    }

    stage('Checkout Code') {
      steps {
        git 'https://github.com/mateossio/docker-pipeline'
      }
    }

  }
}