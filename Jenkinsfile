pipeline{
agent any
tools{
    maven 'Maven'
    }
    stages{
    	stage('Checkout'){
    	steps{
    		git branch:'main',url:'https://github.com/prasadmv-collab/mvnex2.git'
    		}
    	}
    	stage('Build'){
    	steps{
    		sh 'mvn clean package'
    		}
    	}
    	stage('Test'){
    	steps{
    		sh 'mvn test'
    		}
    	}
    	stage('Run Application'){
    	steps{
    		sh 'java -jar target/mvnex2-1.0-SNAPSHOT.jar'
    		}
    	}
    	}
    post{
    	success{
    		echo 'Build success'
    		}
    	failure{
    		echo 'Build failed'
    		}
    	}
    }
