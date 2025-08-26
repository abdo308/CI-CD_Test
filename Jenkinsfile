pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t abdalrhman308/ci-cd_test -f Dockerfile.dev .'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'docker run -e CI=true abdalrhman308/ci-cd_test npm test'
            }
        }
    }
}
