pipeline {
  agent any

  stages {
    stage('Build + SonarQub Analysis') {
      steps {
        sh "./mvnw clean verify sonar:sonar -Dsonar.host.url=http://10.0.0.11:9000 package -DoutputDirectory=/var/shared"
      }
    }
  }
}