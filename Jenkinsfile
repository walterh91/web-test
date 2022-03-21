node{
    def app
        stage('Clone'){
            checkout scm
        }
        stage('crear imagen'){
            echo "crear imagen"
        }
        stage('Correr imagen'){
            sh 'docker run -p 81:80 -d -name web-test1 walterh91/web-nginx:latest'
        }
}
