//pipeline end to end
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
        stage(DockerBuildnPush) {
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
            when {
                branch 'release-*'
            }
            steps {
                echo " Deploying to stage env"
            }
        }
        stage('DeploytoProd') {
            when { 
                //vx.x.x  
                //v1.2.3

                tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}" ,comparator: "REGEXP"
            }
            steps {
                echo " Deploying to prod env"
            }
        }
    }
}
   
