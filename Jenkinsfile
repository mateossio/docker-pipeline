pipeline {
  agent any
  environment {
    DOCKERHUB_CRED = credentials('dockerhub-cred')
  }
  stages {
    stage('Echo test') {
      steps {
        sh 'echo "Hello User:"'
        sh 'echo $USER'
        sh 'echo "Dockerhub cred:"'
        sh 'echo "user ${DOCKERHUB_CRED_USR} passwd ${DOCKERHUB_CRED_PSW} or $DOCKERHUB_PASS"'
      }
    }

    stage('Building Docker Img'){
      steps {
        sh 'docker build -f ./Dockerfile . -t mateofbossio/docker-pipeline:latest'
      }
    }

    stage('Login Dockerhub'){
      steps{
        sh 'docker login -u $DOCKERHUB_CRED_USR -p $DOCKERHUB_CRED_PSW'
      }
    }

    stage('Push Docker img'){
      steps{
        sh 'docker push mateofbossio/docker-pipeline:latest'
      }
    }

  }
}