pipeline {
  agent any
  stages {
    stage('print') {
      steps {
        sh '''echo "this is gahmad"
echo "my name is $NAME"
today date is $date'''
      }
    }

  }
  environment {
    NAME = 'Mukesh'
  }
}