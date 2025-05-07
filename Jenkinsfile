pipeline {
    agent any

    triggers {
        pollSCM 'H/3 * * * *'
    }

    stages {
        stage('Clone'){
             steps {
                git url: 'https://github.com/Satya-Shreya/DevopsEtp.git', branch: 'master'
            }
        }
        stage('Build') {
            
                steps {
                    echo "Building Docker image..."
                    // Build Docker image from Dockerfile
                    sh 'docker build -t my-image-name .'
                    
                    echo "Running Docker container..."
                    // Run Docker container (detached mode)
                    sh 'docker run -d --name my-container -p 8080:80 my-image-name'
                }
            
        }

        stage('Test') {
            steps {
                echo "test stage"
            }
        }

        stage('Deploy') {
            steps {
                echo "deploy stage"
            }
        }
    }
}
