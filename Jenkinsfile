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
      }
    }
    stage('UI Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'I\'m Testing!'
          }
        }
        stage('IE11') {
          steps {
            echo 'Testing IE11'
            sh 'exit 1'
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
      }
    }
    stage('Test Prod') {
      steps {
        echo 'I\'m Testing Production!'
      }
    }
  }
}