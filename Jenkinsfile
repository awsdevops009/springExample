pipeline {
      agent any
	  stages {
	    stage('Build') {
		   steps {
		      sh "rm -rf springExample"
		      sh "git clone https://github.com/awsdevops009/springExample.git"
			  sh "mvn clean "
			  }
             }
		stage('Test') {
		   steps {
		      sh "mvn test -f  springExample"
		      echo "Welcome to Test"
			  }
             }	 
        stage('Deploy') {
		   steps {
		      sh "mvn package -f  springExample"
		      echo "It is going to package the project today"
			  }
             }	     
	}	}
