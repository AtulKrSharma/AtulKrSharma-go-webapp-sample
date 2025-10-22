pipeline {
  agent any
  tools {
    go 'Go Jenkins1.22'
  }

  environment {
    GO111MODULE = 'on'
  }

  stages {
    stage('Test') {
      steps {
        git 'git@github.com:AtulKrSharma/AtulKrSharma-go-webapp-sample.git'
        sh 'go test ./...'
      }

    }
  }
}