pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/cts-devops-as400/pipetest.git', branch: 'master')
      }
    }
    stage('build') {
      steps {
        bat 'mvn package '
      }
    }
  }
}