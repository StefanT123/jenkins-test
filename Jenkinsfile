pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo something'
                sh 'docker ps'
                // script {
                //     docker.image('laradock_workspace_1').withRun('composer --version')
                // }
            }
        }
    }
}
