pipeline {
  agent any
  stages {
    stage('Echo test') {
      steps {
        sh 'echo "Hello User:"'
        sh 'echo $USER'
      }
    }

    stage('Building Docker Img'){
      steps {
        sh 'docker build -f ./Dockerfile . -t mateofbossio/docker-pipeline:latest'
      }
    }

    stage('Login Dockerhub'){
      steps{
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASS'
      }
    }

    stage('Push Docker img'){
      steps{
        sh 'docker push mateofbossio/docker-pipeline:latest'
      }
    }

  }
}