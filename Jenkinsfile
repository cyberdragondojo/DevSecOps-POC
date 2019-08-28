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
        stage('Deploy Web-Server') {
          steps {
            sleep 40
            echo 'Web-Server Deployed Successfully!!'
          }
        }
      }
    }
    stage('Deploy Web-App') {
      steps {
        echo 'Web-Application Deployed Successfully!!'
      }
    }
    stage('DAST') {
      parallel {
        stage('DAST') {
          steps {
            bat 'C:\\Users\\jose\\Documents\\dast\\arachni-1.5.1-0.5.12-windows-x86_64\\bin\\arachni --output-verbose --report-save-path C:\\Users\\jose\\Desktop\\arachni_scans.htm --timeout 00:01:00 http://testfire.net'
          }
        }
        stage('test') {
          steps {
            sleep 15
          }
        }
      }
    }
  }
}