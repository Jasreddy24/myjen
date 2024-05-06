pipeline{
	agent any
	parameters{
	    choice(name: 'ENVIRONMENT',
	      choices: ["DEV", "UAT", "PRD"],
	      description: "Choose the environment to deploy...")
	}

	stages{
	stage("Build"){
	steps{
	echo "Building successfull..."
	}
	}

	stage("DEV-Deploy"){
	when {
	expression {params.ENVIRONMENT == 'DEV'}
	}
	steps{
	echo "I am from the DEV env, Deployed successfully..."
	}
	}

	stage("UAT- Deploy"){
	when {
	expression {params.ENVIRONMENT == 'UAT'}
	}
	steps{
	echo "I am from the UAT env, deployed successfully..."
	}
	}

	stage("PRD- Deploy"){
	when {
	expression {params.ENVIRONMENT == 'PRD'}
	}
	steps{
	echo "I am from PROD, deployed successfully..."
	}
	}
	}
}
