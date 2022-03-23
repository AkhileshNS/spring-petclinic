pipeline {
  agent any

  stages {
    stage('Build + SonarQub Analysis') {
      steps {
        sh "./mvnw clean sonar:sonar package"
      }
    }
  }
}