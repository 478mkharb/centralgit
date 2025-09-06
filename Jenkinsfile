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
      parallel {
        stage('test') {
          agent any
          steps {
            timestamps() {
              echo 'this is a test stage'
              cleanWs()
            }

          }
        }

        stage('test2') {
          steps {
            sh '''df -Th
sudo systemctl status httpd.service'''
          }
        }

      }
    }

  }
  environment {
    NAME = 'Mukesh'
  }
}