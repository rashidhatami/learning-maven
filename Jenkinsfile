pipeline {
   // 
   agent any
    
    stages {
     
        stage ('Checkout') {
          steps {
                git 'https://github.com/rashidhatami/learning-maven.git'
                 }
        }
        stage('Build') {
            agent { docker 'maven:latest' }
            steps {
                sh 'mvn clean package'
               // junit '**/target/surefire-reports/TEST-*.xml' 
		    }
	}

    }
}
