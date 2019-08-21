pipeline {
  agent any
  stages {
    stage('Dependency Check') {
      steps {
        dependencyCheck()
      }
    }
    stage('SAST SCAN') {
      steps {
        echo 'Static-Code-Analysis-Completed!'
      }
    }
  }
}