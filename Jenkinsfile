pipeline{
	agent any
	tools{
	gradle 'Gradle',
	jdk 'JDK'
	}
	
	stages{
	stage('CheckOut'){
	steps{
	git branch:'master', url:'https://github.com/TATIKONDASOWMYA/MyGradleApp01.git}
	}
	stage('Build'){
	steps{
	sh 'gradle build'}
	}
	stage('Test'){
	steps{
	sh 'gradle test'}
	}
	stage('Run'){
	steps{
	sh 'gradle run'}
	}
	}
	post{
	success:{echo 'Build Success'}
	failure:{echo 'Build failure'}
	}
}
