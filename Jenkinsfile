pipeline {
    agent { docker { image 'php' } }
    docker.image('laradock_workspace_1').withRun('composer --version')
    stages {
        stage('build') {
            steps {
                sh 'echo something'
            }
        }
    }
}
