pipeline {
  agent any

  stages {
    stage('SonarQube Analysis') {
      steps {
        sh "./mvnw clean verify sonar:sonar -Dsonar.host.url=http://10.0.0.11:9000"
      }
    }
    stage('Build') {
      sh "./mvnw package"
    }
    stage('Transfer Build') {
      steps {
        sh "mv ${env.WORKSPACE}/target/spring-petclinic-2.6.0-SNAPSHOT.jar /var/shared"
      }
    }
  }
}