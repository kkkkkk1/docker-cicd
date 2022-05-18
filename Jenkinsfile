pipeline {
    agent any
    stages {
		stage ('Prepare){
			steps {
				script {
				checkout scm
					sh "git rev-parse --short HEAD > .git/commit-id"
					commit_id = readFile('.git/commit-id').trim()
				}
			}
		}
        stage('Compile and Build Binary') {
            parallel {
                stage(“dockerbuild”) {
				steps {
					script {
                       def app = docker.build("kkkkkk1/docker-cicd:${commit_id}", './basics')
                     }
					}
				}
            
                stage(“sonar”) {
     			steps {
					sh """
					echo "sonar"
					"""
					}
                }
			}
        }
   
	   stage('docker build/push') {            
			steps {
			   sh """
				echo "push image"
				"""
			}
	   }     
	}
}
