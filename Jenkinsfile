pipeline {
    agent any
    // environment {
    //     BRANCH_NAME = "${env.BRANCH_NAME}"
    // }
    // stages {
    //     stage('checkout') {
    //         steps {
    //             git branch: 'main', credentialsId: 'github-pabbico', url: 'https://github.com/pabbico/jenkins-tutorials.git'
    //         }
    //     }
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
         stage('Main Branch cloning') {
            // when {
            //     branch 'main'
            // }
            steps {
                sh 'docker run -d -p 84:80 main'
            }
        }
    }
}
