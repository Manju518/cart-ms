pipeline {
    agent any 
    stages {
        stage('Build')
        {
            steps{
                echo "Buidling the project"
            }
        }
        stage('CodeAnalysis'){
            steps{
                echo "Running code analysis"

            }
        }
        stage('DockerBuildnPush') {
            steps{
                echo "Building pushing docker image"
            }
        }
        stage('DeploytoDev') {
            steps {
                echo " Deploying to dev env"
            }
        }
        stage('DeploytoTest') {
            steps {
                echo " Deploying to Test env"
            }
        }
        stage('Deploytostage') {
            steps {
                echo " Deploying to stage env"
            }
        }
        stage('DeploytoProd') {
            steps {
                echo " Deploying to prod env"
            }
        }
    }
}
