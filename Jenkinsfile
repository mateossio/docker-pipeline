pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/mateossio/docker-pipeline', branch: 'main')
      }
    }

  }
}