pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh './gradlew wrapper --gradle-version 6.0.1'
        sh './gradlew clean build -P env=prod'
      }
    }

    stage('Clean up') {
      steps {
        deleteDir()
      }
    }

  }
}