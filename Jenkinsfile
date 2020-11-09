pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn compile'
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

    stage('Archival') {
      steps {
        archiveArtifacts '+'
      }
    }

  }
  environment {
    Maven = 'Maven3.6.3'
  }
}