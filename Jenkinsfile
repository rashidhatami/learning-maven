pipeline {
   agent { docker 'maven:latest' }
    
    stages {
     
        stage ('Checkout') {
          steps {
                git 'https://github.com/rashidhatami/learning-maven.git'
                 }
        }
	    stage ('Compile') {
          steps {
                sh 'mvn compile'
                 }
        }
	   
        stage('Package') {
            steps {
                sh 'mvn clean Package'
                
		    }
	}
	    stage('Verify') {
            steps {
                sh 'mvn verify'
                
		    }
	}

    }
}
