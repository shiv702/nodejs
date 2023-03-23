pipeline {
    agent any
    // environment {
    //     BRANCH_NAME = "${env.BRANCH_NAME}"
    // }
    stages {
        stage('checkout') {
            steps {
                git branch: 'main', credentialsId: '33f3bdae-c4a0-4dea-aaa8-24a21faf5a7d', url: 'https://github.com/shiv702/nodejs.git'
            }
        }
        // stage('Test Branch') {
        //     when {
        //         branch 'test'
        //     }
        //     steps {
        //         sh 'echo "Test branch commit made!"'
        //     }
        // }
        stage('Main Branch cloning') {
            // when {
            //     branch 'main'
            // }
            steps {
                sh 'docker build -t main .'
            }
        }
        {
            // when {
            //     branch 'main'
            // }
            steps {
                sh 'docker run -d -p 84:80 main'
            }
        }
    }
}
