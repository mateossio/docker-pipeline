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
        git credentialsId: 'git', url: 'git@github.com:jenkinsci/git-client-plugin.git'
      }
    }

  }
}