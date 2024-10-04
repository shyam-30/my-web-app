pipeline{
  agent any 
  environment{
    IMAGE_NAME = 'shyam30/my-web-app'
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
    stage('run docker container'){
      steps{
        script{
          docker.image("${IMAGE_NAME}").run('-p 3000:3000')
        }
      }
    }
  }
}
