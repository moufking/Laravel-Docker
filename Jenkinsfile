pipeline {
    agent any

    stages {
        stage('Build image') {
        app = docker.build("nginx:latest")
            }
         stage('Test image') {
        docker.image('xavki/nginx').withRun('-p 80:80') { c ->
        sh 'docker ps'
        sh 'curl localhost'
	     }
    }

        }
    }

