pipeline {
  agent any

  tools {
    go 'Go Jenkins1.22'
  }

  environment {
    GO111MODULE = 'on'
  }

  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/AtulKrSharma/AtulKrSharma-go-webapp-sample.git'
      }
    }

    stage('Test') {
      steps {
        sh 'go test ./...'
      }
    }

    stage('Build') {
      steps {
        sh 'go build .'
      }
    }

    stage('Run') {
      steps {
        // Example: Run binary briefly to confirm it starts
        sh '''
          ./go-webapp-sample &
          sleep 5
          pkill go-webapp-sample
        '''
      }
    }
  }
}
