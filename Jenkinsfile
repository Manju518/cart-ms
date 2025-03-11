pipeline {
    agent any
    stages {
        stage ('DockerBuildPush') {
            steps {
                sh "docker pull nginx"
                echo "***printing the images****"
                sh "docker images"
                sh "Docker tag nginx manju518/nginxdevops:b6"
                sh "docker push manju518/nginxdevops:b6"
            }
        }
    }
}
