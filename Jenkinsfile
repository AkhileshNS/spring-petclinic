pipeline {
  agent any

  stages {
    stage('Build + SonarQub Analysis') {
      steps {
        sh "./mvnw clean verify sonar:sonar -Dsonar.host.url=$SONAR_HOST package"
      }
    }
  }
}