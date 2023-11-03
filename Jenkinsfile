pipeline {
  agent any
  stages {
    stage('Checkout Repo') {
      steps {
        git(url: 'https://github.com/mateossio/docker-pipeline.git', branch: 'master')
      }
    }

  }
}