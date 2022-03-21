pipeline{
    agent any
    environment{
        GIT_TAG = sh(returnStdout: true, script: "git rev-parse --short=10 HEAD").trim()
    }
    stages{
        stage('Clone Repo'){
            steps{
                checkout scm
            }
        }
        stage('Crear imagen'){
            steps{
                sh 'docker build -t walterh91/web-nginx:$GIT_TAG .'
            }
        }
    }
}