node{
    def app
        stage('Clone'){
            checkout scm
        }
        stage('crear imagen'){
            sh 'docker build -t walterh91/web-nginx:$(git rev-parse --short=10 HEAD) .'
        }
        stage('Detener contenedor si existiese'){
            sh 'docker rm -f web-test'
        }
        stage('Correr imagen'){
            sh 'docker run -p 81:80 -d --name web-test walterh91/web-nginx:$(git rev-parse --short=10 HEAD)'
        }
    
}
