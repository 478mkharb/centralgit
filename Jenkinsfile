pipeline {
  agent any
  stages {
    stage('print') {
      steps {
        sh '''echo "this is gahmad"
echo "my name is $NAME"
date
ls -al
touch file.txt
        ls -al'''
      }
    }

  }
  environment {
    NAME = 'Mukesh'
  }
}
