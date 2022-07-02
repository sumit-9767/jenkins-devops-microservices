//Declarative Method
pipeline{
	agent any
	//agent { docker{ image  'node:current-alpine3.15' } }
	stages{
		stage('Build'){
			steps{
				//sh 'node --version'
				echo "$PATH"
				echo "Build"
				echo "$env.BUILD_NUMBER-$env.BUILD_NUMBER"
				echo "$env.BUILD_ID"
				echo "$env.JOB_NAME"
			}

		}
		stage('Test'){
			steps{

				echo "test"

			}

		}
		stage('Intergration Test'){
			steps{
				echo "Intergration Test"
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

