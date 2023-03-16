pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/edidiong-john/curriculum-app', branch: 'dev')
      }
    }

    stage('Log') {
      parallel {
        stage('Test') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit Tests / Shell Script') {
          steps {
            sh 'cd curriculum-front && npm i & npm run test:unit'
          }
        }

      }
    }

  }
}