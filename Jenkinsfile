pipeline {
  agent any
  stages {
    stage('Push Jenkinsfile') {
      steps {
        git(url: 'https://github.com/dave-cmd/curriculum-app', branch: 'dev')
      }
    }

    stage('Logs') {
      steps {
        sh 'ls -la'
      }
    }

  }
}