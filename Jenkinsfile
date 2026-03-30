node {
    stage('Checkout') {
        git branch: 'main', url: 'https://github.com/zdeo4/laravel.git'
    }

    stage("Build") {
        docker.image('composer:2').inside('-u root') {
            sh 'composer install'
        }
    }

    stage("Testing") {
        docker.image('ubuntu').inside('-u root') {
            sh 'echo "Ini adalah test"'
        }
    }

    stage("Deploy") {
        docker.image('agung3wi/alpine-rsync:1.1').inside('-u root') {
            echo "Deploy skipped sementara"
        }
    }
}
