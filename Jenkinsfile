pipeline {
  agent any

  stages {
    stage('Build + SonarQub Analysis') {
      steps {
        sh "mvn clean sonar:sonar package"
      }
    }
  }
}