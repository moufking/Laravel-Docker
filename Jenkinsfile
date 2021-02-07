node {
        docker.image('nginx:latest').withRun('-p 80:82') { c ->

        sh 'docker ps'

        sh 'curl localhost'

    }
}
