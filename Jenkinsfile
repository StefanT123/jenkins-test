pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo something'
                sh 'docker exec laradock_workspace_1 vendor/bin/phpunit'
            }
        }
    }
}
