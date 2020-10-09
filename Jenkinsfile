pipeline {
    agent any
    stages {
        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }
        // stage('Test application') {
        //     steps {
        //         sh 'npm test'
        //     }
        // }
        stage('Build application') {
            steps {
                sh 'npm build'
            }
        } 
        stage('Install serve') {
            steps {
                sh 'npm i -g serve'
            }
        }
        stage('Deploy') {
            steps {
                sh 'serve -s build'
            }
        }
    }
}