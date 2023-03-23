pipeline {
    agent any

    stages {
        stage('Main Branch cloning') {
            steps {
                git branch: 'main', credentialsId: '33f3bdae-c4a0-4dea-aaa8-24a21faf5a7d', url: 'https://github.com/shiv702/nodejs.git'
            }
        }
        stage('Build') {
            steps {
                sh 'sudo -A chown root:root /var/run/docker.sock'
                sh 'sudo docker build -t main .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 84:80 main'
            }
        }
    }
}
