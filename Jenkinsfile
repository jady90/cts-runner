pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
				bat "docker pull jadyjdjady1990/cts-docker"
			}
		}
		stage("Start Grid"){
			steps{
				bat "docker-compose up -d hub chrome edge"
			}
		}
		stage("Run Test"){
			steps{
				bat "docker-compose up myinsurance"
			}
		}
	}
	post{
		always{
			bat "docker-compose down"
		}
	}
}
