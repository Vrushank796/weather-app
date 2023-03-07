pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/Vrushank796/weather-app', branch: 'main')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit tests') {
          steps {
            sh 'npm cache clean --force && npm fund && npm audit fix --force && npm i --package-lock-only && npm audit fix --force && npm run test'
          }
        }

      }
    }

  }
}