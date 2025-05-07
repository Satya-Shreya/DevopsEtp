pipeline{
    agent any
    tirggers{
        pollSCM 'H/3 * * * *'
    }
    stages{
        stage('Build'){
            echo "build stage"

            sh 'docker build -t html_image .'

            sh 'docker run -it -d --name website -p 8081:80 html_image'
        }
        stage('Test'){
            echo "test stage"
        }
        stage('Deploy'){
            echo "deploy stage"
        }
    }
}