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
        git 'https://github.com/AtulKrSharma/AtulKrSharma-go-webapp-sample.git'
        sh 'go test ./...'
      }
      stage('Build') {
        steps {
          git 'https://github.com/AtulKrSharma/AtulKrSharma-go-webapp-sample.git'
          sh 'go build .'
        }
        stage('Run') {
          steps {
            sh 'cd /var/lib/jenkins/workspace/Om && go-webapp-sample &'
          }

        }
      }
    }