node{
    def app
        stage('Clone'){
            checkout scm
        }
        stage('get code commit'){
            GIT_COMMIT= sh (script: 'git log -1 --pretty=%H')
            echo ${GIT_COMMIT}
        }
        stage('crear imagen'){
            
            sh 'docker build -t walterh91/web-nginx:${GIT_COMMIT} .'
        }
        stage('Detener contenedor si existiese'){
            sh 'docker rm -f web-test'
        }
        stage('Correr imagen'){
            sh 'docker run -p 81:80 -d --name web-test walterh91/web-nginx:${GIT_COMMIT}'
        }
}
