pipeline {
  agent any
  stages {
    stage('Echo test') {
      steps {
        sh 'echo "Hello World"'
        sh 'echo $(ls -l)'
      }
    }

    stage('Checkout Code') {
      steps {
        git url: 'git@github.com:jenkinsci/git-client-plugin.git'
      }
    }

  }
}