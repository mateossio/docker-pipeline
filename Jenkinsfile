pipeline {
  agent any
  stages {
    stage('Echo test') {
      steps {
        sh 'echo "Hello World"'
        sh 'echo $(ls -l)'
      }
    }

    stage('Installing and Starting App') {
      steps {
        sh 'npm i'
        sh 'npm start'
      }
    }

  }
}