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
    stage('Test') {
      steps {
        echo 'I\'m Testing!'
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
