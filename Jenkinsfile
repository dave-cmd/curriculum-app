pipeline {
  agent any
  stages {
    stage('Push Jenkinsfile') {
      steps {
        git(url: 'https://github.com/dave-cmd/curriculum-app', branch: 'dev')
      }
    }

    stage('Logs') {
      parallel {
        stage('Logs') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Frontend Unit Tests') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}