#!/usr/bin/env groovy

pipeline {
  agent any

  stages {
    stage('Test') {
      steps {
        sh 'gradle wrapper --gradle-version 5.1.1'
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
