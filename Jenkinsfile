pipeline {
	agent{
	label 'mens-slave'
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/grras/appfiles/apache-maven-3.9.6/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/slave.war /home/grras/appfiles/apache-tomcat-9.0.85/webapps'
			}}	
}}

