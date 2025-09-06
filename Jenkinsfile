pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''echo "this is pipelineuser"
        echo "my name is $NAME"
        date
        ls -al
        touch file.txt
        ls -al
        pwd'''
      }
    }

    stage('test') {
      agent any
      steps {
        timestamps() {
          echo 'this is a test stage'
          cleanWs(cleanWhenSuccess: true)
        }

      }
    }

  }
  environment {
    NAME = 'Mukesh'
  }
}