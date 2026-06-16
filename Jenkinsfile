pipeline{

agent any

tools{
maven 'Maven'

}

	stages{
	
	stage('checkout')
	{
	steps{
	git branch:'main',url:'https://github.com/prasadmv-collab/mvnex2.git'
	}
	}
	
	
	stage('Build')
	{
	steps{
	sh 'mvn clean package'
	}
	}
	
	stage('Test')
	{
	steps{
	sh 'mvn test'
	}
	}
	
	
	stage('Run application')
	{
	steps{
	sh 'java -jar target/mvnex2-1.0-SNAPSHOT.jar'
	}
	}
	
	}
	
	post{
	
	success{
	
		echo 'Build successfully done'
	}
	
	failure{
	
		echo 'Build failed retry'
	}
	
	}
}
	
