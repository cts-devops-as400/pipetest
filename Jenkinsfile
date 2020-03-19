pipeline {
  agent any
  stages {
    stage('unit test') {
      steps {
        bat 'mvn test'
      }
    }
    //this is new branch
    stage('build') {
      steps {
        bat 'mvn package'
      }
    }
    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            bat 'mvn tomcat9:deploy'
          }
        }
        stage('sonar scan') {
          steps {
            bat 'mvn sonar:sonar \\   -Dsonar.projectKey=fstsonar \\   -Dsonar.host.url=http://localhost:9000 \\   -Dsonar.login=1c4bb832eae98daf18e8a0c4ae49f58f75cf6415'
          }
        }
      }
    }
  }
}
