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
        archiveArtifacts '*'
        archiveArtifacts(onlyIfSuccessful: true, allowEmptyArchive: true, artifacts: '*')
      }
    }

  }
  environment {
    Maven = 'Maven3.6.3'
  }
}