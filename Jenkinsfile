pipeline {
  agent any
  stages {
    stage('SAST') {
      steps {
        withSonarQubeEnv(credentialsId: '0068e3eec2d0d97675155b2d147c1a37f10ce04a', installationName: 'https://sonarcloud.io')
      }
    }
  }
}