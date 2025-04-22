pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package -nsu -DskipMunitTests'
      }
    }

    stage('SonarQuebe') {
      steps {
        withSonarQubeEnv 'SonarQube'
      }
    }

  }
}