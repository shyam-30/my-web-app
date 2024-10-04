pipeline{
  agent any 
  environment{
    IMAGE_NAME = 'shyam30/my-web-app'
    DOCKER_CREDENTIALS = 'dockerid'
  }
  stages{
    stage('cclone repository'){
      steps{
        echo "cloning the repository"
      }
    }
    stage('docker build image'){
      steps{
        script{
          docker.build("${IMAGE_NAME}")
        }
      }

    }
    stage('run docker container'){
      steps{
        script{
          docker.image("${IMAGE_NAME}").run('-p 3000:3000')
        }
      }
    }
    stage('docker push image'){
      steps{
        script{
          withCredentials([usernamePassword(credentialsId: DOCKER_CREDENTIALS, usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]){
            sh '''
            #!/bin/bash
            echo "login"
            echo "$DOCKER_PASSWORD" | docker login -u "$DOCKER_USERNAME" --password-stdin
            echo "pushing docker image"
            docker push ${IMAGE_NAME}
            '''
          }
        }
      }
    }
  }
}
