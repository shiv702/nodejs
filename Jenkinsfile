pipeline {
    agent any

    stages {
        stage('Main Branch cloning') {
            steps {
                sh 'docker build -t main .'
            }
        }
        stage('Run container') {
            steps {
                sh 'docker run -d -p 84:80 main'
            }
        }
    }
}
