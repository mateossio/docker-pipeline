pipeline {
  agent any
  enviroment {
    DOCKERHUB_USER = credentials('DOCKERHUB_USER')
    DOCKERHUB_PASS = credentials('DOCKERHUB_PASS')
  }
  stages {
    stage('Echo test') {
      steps {
        sh 'echo "Hello User:"'
        sh 'echo $USER'
        sh 'echo "Dockerhub cred:"'
        sh 'echo "user ${DOCKERHUB_USER} passwd ${DOCKERHUB_PASS} or $DOCKERHUB_PASS"'
      }
    }

    stage('Building Docker Img'){
      steps {
        sh 'docker build -f ./Dockerfile . -t mateofbossio/docker-pipeline:latest'
      }
    }

    stage('Login Dockerhub'){
      steps{
        sh 'docker login -u ${DOCKERHUB_USER} -p ${DOCKERHUB_PASS}'
      }
    }

    stage('Push Docker img'){
      steps{
        sh 'docker push mateofbossio/docker-pipeline:latest'
      }
    }

  }
}