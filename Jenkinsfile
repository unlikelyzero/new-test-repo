pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'I\'m building!'
      }
    }
    stage('Deploy Test Environment') {
      steps {
        echo 'I\'m Testing!'
        sleep 3
      }
    }
    stage('UI Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'I\'m Testing!'
            sleep 3
          }
        }
        stage('IE11') {
          steps {
            echo 'Testing IE11'
            sh 'exit 0'
          }
        }
        stage('Chrome') {
          steps {
            echo 'Testing in Chrome'
          }
        }
        stage('Firefox') {
          steps {
            echo 'Ffox'
          }
        }
      }
    }
    stage('Deploy Production') {
      steps {
        echo 'Deploy'
        sleep 3
      }
    }
    stage('Test Prod') {
      steps {
        echo 'I\'m Testing Production!'
      }
    }
  }
}