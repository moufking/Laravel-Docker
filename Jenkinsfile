pipeline {
agent any

stages {
    stage('Build') {
        steps {
            sh 'composer install --no-interaction'
            sh 'npm run prod'
            sh 'run some other commands to compile assets'
        }
    }
    stage('Test') {
        steps {

            sh './vendor/bin/phpunit'

        }
    }
    stage('Deploy') {
        steps {

        sh 'ssh -o StrictHostKeyChecking=no prod_server_user@prod_server_ip "cd /path/to/your/app_code; \
            git pull origin master; \
            composer install --no-interaction --no-dev; \
            php artisan migrate --force; \
            php artisan cache:clear; \
            php artisan config:cache "'
            // and so on depending on your requirements
        
                
            }
    }
}
}
