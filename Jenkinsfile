pipeline {
    agent any 
	stages {
	 stage('git') {
	  steps{
	git credentialsId: 'e03681b0-f2be-482c-83d9-4650b2a289d7', url: 'https://github.com/VelpulaAkkini/maven-project.git'
	}
	}
	stage('validate code') {
	 steps {
	sh 'mvn clean validate'
	}
	 }
	stage('test code') {
	 steps {
	  sh 'mvn clean test'
	 }
	} 
	 stage('compile code') {
	   steps {
	     sh 'mvn clean compile'
	   }
	 } 
	  stage('deploy code') {
	   steps {
	    sh 'mvn clean package'
	   }
	  }
	
 	 }

}
