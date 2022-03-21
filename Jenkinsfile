pipeline{
    agent any
    environment{
        GIT_TAG = sh(returnStdout: true, script: "git rev-parse --short=10 HEAD").trim()
    }
    stages{
        stage('Clone Repo'){
            steps{
                echo $GIT_TAG
            }
        }
    }
}