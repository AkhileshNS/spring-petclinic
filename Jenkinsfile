pipeline {
  agent any

  stages {
    stage('SonarQube Analysis') {
      steps {
        withSonarQubeEnv("SonarQube Scanner") { 
          sh './mvnw org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
        }
      }
    }
    stage('Build') {
      steps {
        sh "./mvnw package"
      }
    }
  }
}