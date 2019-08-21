pipeline {
  agent any
  stages {
    stage('SAST SCAN') {
      parallel {
        stage('SAST SCAN') {
          steps {
            echo 'Static-Code-Analysis-Completed!'
          }
        }
        stage('IMAGE SCAN') {
          steps {
            bat(script: 'START C:\\Users\\jose\\Documents\\Depcheck\\dependency-check\\bin -s C:\\Users\\jose\\Documents\\auto\\auto-ossec-master', encoding: 'UTF-8', returnStatus: true, returnStdout: true)
          }
        }
      }
    }
  }
}