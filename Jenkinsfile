pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo something'
            }
        }
        stage('test') {
            steps {
                sh 'docker exec laradock_workspace_1 vendor/bin/phpunit'
            }
        }
    }
}
