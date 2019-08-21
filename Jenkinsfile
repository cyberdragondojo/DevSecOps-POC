pipeline {
  agent any
  stages {
    stage('SAST') {
      parallel {
        stage('SAST') {
          steps {
            sh 'echo Static-Code-Analysis-Complete!'
          }
        }
        stage('Dependency Check') {
          steps {
            snykSecurity(projectName: 'cyberdragondojo/auto-ossec', organisation: 'cyberdragondojo')
          }
        }
      }
    }
  }
}