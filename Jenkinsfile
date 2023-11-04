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
        sh 'sudo docker build -f ./Dockerfile . -t mateofbossio/docker-pipeline:latest'
      }
    }

    stage('Login Dockerhub'){
      steps{
        sh 'sudo docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASS'
      }
    }

    stage('Push Docker img'){
      steps{
        sh 'sudo docker push mateofbossio/docker-pipeline:latest'
      }
    }

  }
}