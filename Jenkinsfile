pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git "https://github.com/Manoharr108/6webapp"
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean install'
			}
		}
		stage('Deploy'){
			steps{
				sh 'ansible-playbook ansible/deploy.yml  -i ansible/hosts.ini'
			}
		}
	}
}
		
