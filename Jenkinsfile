pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn build'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Package') {
      steps {
        sh 'mvn package'
      }
    }

  }
  environment {
    Maven = 'Maven3.6.3'
  }
}