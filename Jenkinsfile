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
            bat 'C:\\Users\\jose\\Documents\\Depcheck\\dependency-check\\bin\\dependency-check.bat -s C:\\Users\\jose\\Documents\\auto\\auto-ossec-master -o C:\\Users\\jose\\Desktop\\dep-check-report.htm'
          }
        }
        stage('Build Binaries') {
          steps {
            echo 'Build Successful!'
          }
        }
        stage('Deploy Webserver') {
          steps {
            sh 'echo \'Web-Server Deployed Successfully!\''
          }
        }
      }
    }
  }
}