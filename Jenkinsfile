node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("laravel/l8")
    }

    stage('Test image') {
        sh 'docker images'
    }
}
