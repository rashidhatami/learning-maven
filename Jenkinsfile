pipeline {
    agent {
        docker {
            image 'maven:latest'
            args '-v /root/.m2:/root/.m2'
        }
    }
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
        stage('Test') { 
            steps {
                sh 'mvn test' 
            }
        }
        stages {
        stage('Package') {
            steps {
                sh 'mvn package'
            }
      }
   
}
