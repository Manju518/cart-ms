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
            options{
                timeout(time: 300, unit: 'SECONDS')
            }
            input {
                message "Doing prod deployments?"
                ok 'yes'
                submitter 'manju518,ramdev'
            }
            steps {
                echo " Deploying to prod env"
            }
        }
    }
}
