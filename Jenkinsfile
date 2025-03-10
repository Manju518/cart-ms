pipeline{
    agent any
    stages{
        stage('Build') {
            steps{
                echo "***Building the application****"
             }
            
        }
        stage('Sonar') {
            steps{
                echo "***scanning the application***"
            }
        }
        stage('Docker'){
            steps{
                echo "***Building the docker image***"
            }
        }
        stage('K8Deploy') {
            steps{
                echo "Deploy using K8"
            }
        }
    }
}
