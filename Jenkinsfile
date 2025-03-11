ppipeline {
    agent any
    stages {
        stage ('Dockerbuildpush') {
            steps {
                sh "docker pull nginx"
                echo "***printing the images****"
                sh "docker images"
            }
        }
    }
}
