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
      }
    }

    stage('Building Docker Img'){
      steps {
        sh 'docker build -f ./Dockerfile . -t docker push mateofbossio/docker-pipeline:latest'
      }
    }

    steps('Login Dockerhub'){
      steps{
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASS'
      }
    }

    steps('Push Docker img'){
      steps{
        sh 'docker push mateofbossio/docker-pipeline:latest'
      }
    }

  }
}