//Declarative Method
pipeline{
	//agent any
	agent {
		docker{
			image  'maven:3.6.3'
		}
	}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				echo "Build"
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

