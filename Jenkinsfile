pipeline {
    agent any
    environment {
        DOCKER_REPO = "manju518/nginxdevops"
    }
    stages {
        stage('Docker Build and Push') {
            steps {
                sh "docker pull nginx"
                echo "*** Printing the images ***"
                sh "docker images"

                echo "*** Tagging the image ***"
                sh "docker tag nginx ${DOCKER_REPO}:b6"

                echo "*** Logging in to Docker Hub ***"
                withCredentials([usernamePassword(credentialsId: 'dockerhub_creds', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
                    sh "echo ${DOCKER_PASS} | docker login -u ${DOCKER_USER} --password-stdin"
                }

                echo "*** Pushing the image to Docker Hub ***"
                sh "docker push ${DOCKER_REPO}:b6"
            }
        }
    }
}
