pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/gnaanesh-ks/2-Tier-aws-Docker-Jenkins.git',
                    branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'docker compose build'
            }
        }


        stage('Done') {
            steps {
                echo 'App is running on port 5000'
            }
        }
    }

    post {
        failure {
            echo 'Build failed!'
        }
    }
}
