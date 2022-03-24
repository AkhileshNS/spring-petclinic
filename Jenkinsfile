pipeline {
  agent any

  stages {
    stage('Build + SonarQub Analysis') {
      steps {
        sh "./mvnw clean verify sonar:sonar -Dsonar.host.url=http://10.0.0.11:9000 package"
      }
    }
    stage('Transfer Build') {
      steps {
        sh "mv /var/lib/jenkins/workspace/spring-petclinic_main/target/spring-petclinic-2.6.0-SNAPSHOT.jar /var/shared/spring-petclinic.jar"
      }
    }
  }
}