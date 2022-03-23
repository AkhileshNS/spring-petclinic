pipeline {
  agent any

  stages {
    stage('Build + SonarQub Analysis') {
      steps {
        sh "./mvnw clean sonar:sonar package -Dsonar.host.url=http://10.0.0.11:9000"
      }
    }
  }
}