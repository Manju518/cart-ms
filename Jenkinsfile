pipeline{
    agent any
    stages{
        stage('DeployToDev'){
            steps {
                echo "Deploying to Dev"
            }
        }
        stage('DeployToProd') {
            when{
                //branch condition
                expression {BRANCH_NAME ==~/(production|staging)/ }
            }
            steps {
            
            echo "Deploying to Prod env"
            }
        }
    }
}
