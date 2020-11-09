pipeline{
    agent any
    tool {
        Maven3.6.3
    } 
stages {
        stage('Build') {
            steps   {
                echo 'Building..'
                sh mvn compile
                    }
            }//Build
       
        stage('Test') {
            steps {
                echo 'Testing'
                sh mvn test
                    }
                }//Testing
        stage('Package') {
            steps {
                echo 'Packaging.'
                sh mvn package
            }
        }//Package
    }//stages
}//pipeline
