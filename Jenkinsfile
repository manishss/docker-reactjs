
pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'git@github.com:manishss/docker-reactjs.git', branch:'dev'
      }
    }
    
      stage("Build image") {
            steps {
                script {
                    myapp = docker.build("myapp/v1:${env.BUILD_ID}")
                }
            }
        }
