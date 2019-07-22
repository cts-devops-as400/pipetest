pipeline {
  agent any
  stages {
    stage('unit test') {
      steps {
        bat 'mvn test'
      }
    }
    stage('build') {
      steps {
        bat 'mvn package'
      }
    }
    stage('deploy') {
      steps {
        bat 'mvn tomcat9:deploy'
      }
    }
  }
}