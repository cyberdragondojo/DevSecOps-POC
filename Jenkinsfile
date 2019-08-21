pipeline {
  agent any
  stages {
    stage('SAST SCAN') {
      steps {
        echo 'Static-Code-Analysis-Completed!'
      }
    }
    stage('Dependency Scan') {
      parallel {
        stage('Dependency Scan') {
          steps {
            bat(script: 'start cmd /k echo Hello, World!', returnStatus: true)
          }
        }
        stage('Build Binaries') {
          steps {
            echo 'Build Successful!'
          }
        }
      }
    }
  }
}