pipeline {
    agent { docker { image 'php' } }
    stages {
        stage('build') {
            steps {
                sh 'echo something'

                script {
                    docker.image('laradock_workspace_1').withRun('composer --version')
                }
            }
        }
    }
}
