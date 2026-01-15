pipeline {
    agent any

    environment {
        IMAGE_NAME = "react-vite-app"
        CONTAINER_NAME = "react-vite-container"
    }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/MamthaKSunilkumar/CS8_demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
<<<<<<< HEAD
                sh 'docker build -t $IMAGE_NAME .'
=======
                bat 'npm install'
>>>>>>> 1ec3edabd7263e45824e6b7cddda6af29724ddaf
            }
        }

        stage('Stop Old Container') {
            steps {
<<<<<<< HEAD
                sh '''
                docker stop $CONTAINER_NAME || true
                docker rm $CONTAINER_NAME || true
                '''
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker run -d \
                -p 5173:5173 \
                --name $CONTAINER_NAME \
                $IMAGE_NAME
                '''
=======
                bat 'npm run build'
>>>>>>> 1ec3edabd7263e45824e6b7cddda6af29724ddaf
            }
        }
    }

    post {
        success {
            echo 'React app deployed using Docker successfully 🎉'
        }
        failure {
            echo 'Deployment failed ❌'
        }
    }
}
