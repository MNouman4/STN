pipeline {
  agent any
  environment {
    DOCKER_TAG = getDockerTag()
  }
  stages {
    stage("Building Docker Image")
    steps {
      sh "docker build -t nouman74/stn:DOCKER_TAG"
    }
  }
}

def getDockerTag(){
  def tag = sh script: 'git rev-parse HEAD', returnStdout: true 
}
