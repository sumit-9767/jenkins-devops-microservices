//Declarative Method
pipeline{
	agent any
	//agent { docker{ image  'node:current-alpine3.15' } }
	environment{
		//dockerHome = tool 'myDocker'
		mavenHome = tool 'MyMaven'
		PATH = "$mavenHome/bin:$PATH"
	
	}
	stages{
		stage('Checkout'){
			steps{
				sh 'mvn --version'
				//sh 'docker version'
				echo "$PATH"
				echo "Build"
				echo "$env.BUILD_NUMBER-$env.BUILD_NUMBER"
				echo "$env.BUILD_ID"
				echo "$env.JOB_NAME"
			}

		}
		stage('Compile'){
			steps{
				sh "mvn clean compile"  		//compile code
			}
		}

		stage('Test'){
			steps{

				sh "mvn test"

			}

		}
		stage('Intergration Test'){
			steps{
				sh "mvn failesafe: integration-test failesafe:verify"
			}

		}
	}
	post{
		always{
			echo 'I Run Always'
		}
		success{
			echo 'I Run Success'
		}
		failure{
			echo 'I Run fail'
		}
	}
}








// git add * git commit -m git push -u origin main


//Scripted old method 
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Intergration Test') {
// 		echo "Intergration Test"
// 	}
// }

