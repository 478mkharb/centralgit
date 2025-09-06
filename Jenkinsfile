pipeline {
  agent any
  stages {
    stage('print') {
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

  }
  environment {
    NAME = 'Mukesh'
  }
}
