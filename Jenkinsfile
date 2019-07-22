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
        bat 'copy C:\\Program Files (x86)\\Jenkins\\workspace\\fstpipeline_master\\target\\*.war  C:\\Program Files\\Apache Software Foundation\\Tomcat 9.0\\webapps'
      }
    }
  }
}