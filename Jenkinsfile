node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("laravel8")
    }

    stage('Test image') {
        docker.image('laravel8').withRun('-p 80:82') { c ->
        sh 'docker ps'
        sh 'curl localhost'
	     }
    }
}
