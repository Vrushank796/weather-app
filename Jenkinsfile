pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/Vrushank796/weather-app', branch: 'main')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

  }
}