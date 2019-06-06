pipeline {
    agent { docker { image 'php' } }
    stages {
        stage('build') {
            steps {
                sh 'php --version'
                // sh 'vendor/bin/phpunit'
                sh 'ls -la'
            }
        }
    }
}
