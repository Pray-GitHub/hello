pipeline {
  agent any
  tools{
       maven 'maven363' 
    }
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
        archiveArtifacts(onlyIfSuccessful: true, artifacts: '*/*.jar')
      }
    }

  }
  
}
