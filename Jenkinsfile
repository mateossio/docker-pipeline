pipeline {
  agent any
  environment {
    DOCKERHUB_CRED = credentials('dockerhub-cred')
  }
  stages {
    stage('Build Artifacts') {
      steps {
        sh 'echo "Building:"'
      }
    }

    stage('Test Artifacts') {
      steps {
        sh 'echo "Testing:"'
      }
    }

    stage('Build Docker Img'){
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