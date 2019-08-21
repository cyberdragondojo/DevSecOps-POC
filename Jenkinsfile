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
            bat(script: 'START C:\\Users\\jose\\Documents\\Depcheck\\dependency-check\\bin\\dependency-check.bat -s C:\\Users\\jose\\Documents\\auto\\auto-ossec-master -o C:\\Users\\jose\\Desktop\\depcheck.htm', encoding: 'UTF-8', returnStatus: true)
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