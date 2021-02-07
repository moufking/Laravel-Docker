node {
        docker.image('nginx:latest').withRun('-p 80:80') { c ->

        sh 'docker ps'

        sh 'curl localhost'

    }
}
