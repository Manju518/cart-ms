pipeline{
    agent any
    stages{
        stage('Build')
        {
            steps{
                echo "Building the application"
            }
        }
    }
    post {
        success{
            echo "post ******* success is triggered"
        }
        failure {
            echo "post******failur is triggered"
        }
        always{
            echo "post *** always is triggered"
        }
    }
}
