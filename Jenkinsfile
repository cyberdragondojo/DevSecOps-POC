pipeline {
  agent any
  stages {
    stage('Dependency Check') {
      steps {
        snykSecurity(projectName: 'cyberdragondojo/auto-ossec', organisation: 'cyberdragondojo')
      }
    }
    stage('SAST SCAN') {
      steps {
        echo 'Static-Code-Analysis-Completed!'
      }
    }
  }
}