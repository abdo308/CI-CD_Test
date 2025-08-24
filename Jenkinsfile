pipeline {
    agent {

        label 'docker'
    }

    stages{
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t abdalrhman308/ci-cd_test -f Dockerfile.dev .'
                }
            }
        }
        stage('Run Tests') {
            steps {
                script {
                    sh 'docker run abdalrhman308/ci-cd_test npm test'
                }
            }
        }


    }


}