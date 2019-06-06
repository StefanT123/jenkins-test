pipeline {
    agent { docker { image 'php' } }
    stages {
        stage('build') {
            steps {
                sh 'docker exec laradock_workspace_1 vendor/bin/phpunit'
            }
        }
    }
}
