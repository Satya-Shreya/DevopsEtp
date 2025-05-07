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
                steps {
                    echo "Building Docker image..."
                    // Build Docker image from Dockerfile
                
                }
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
