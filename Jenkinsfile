node{
    def app
        stage('Clone'){
            checkout scm
        }
        stage('crear imagen'){
            echo "crear imagen"
        }
        stage('Correr imagen'){
            docker.image('walterh91/web-nginx').withRun('-p 80:80')
        }
}
