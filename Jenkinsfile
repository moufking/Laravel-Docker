node{
  def app
    
    stage('Build image') {
        app = docker.build("laravel/l8")
    }

    stage('Test image') {
      sh 'docker images'
    }
    
    stage('listing processus') {
         sh 'docker ps'
    }
}
