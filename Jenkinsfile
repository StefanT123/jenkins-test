pipeline {
    agent { docker { image 'php' } }
    stages {
        stage('build') {
            steps {
                sh 'php --version'
                sh 'ls -la'
                sh 'LC_ALL=C.UTF-8 add-apt-repository -y ppa:ondrej/php'
                sh 'apt-get update'
                sh 'apt-get install -y php7.3 php7.3-xdebug php7.3-xsl php7.3-dom php7.3-zip php7.3-mbstring'
                sh 'php -r "copy(\'https://getcomposer.org/installer\', \'composer-setup.php\');"'
                sh 'php composer-setup.php --install-dir=/usr/local/bin --filename=composer'
                sh 'php composer-setup.php'
                sh 'php -r "unlink(\'composer-setup.php\');"'
                sh 'composer --version'
                sh 'chown -R $USER:$USER ~/.composer/'
                sh 'composer install'
                sh 'vendor/bin/phpunit'
            }
        }
    }
}
