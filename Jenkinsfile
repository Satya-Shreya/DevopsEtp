pipeline{
    agent any
    triggers{
        pollSCM 'H/3 * * * *'
    }
    stages{
        stage('Build'){

           script{
             echo "build stage"

            sh 'docker build -t html_image .'

            sh 'docker run -it -d --name website -p 8081:80 html_image'
           }
           stage('Test'){
            steps{
                echo "test stage"
            }
           }
           stage('Deploy'){
            steps{
                echo "deploy stage"
            }
           }
        }
      
    }
}