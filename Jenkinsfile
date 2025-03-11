pipeline{
    agent any
    environment{
        DEPLOY_TO ='production'
    }
    stages{
        stage('DeploytoDev') {
            steps {
            echo "deploying to Dev env"
            }
        }
        stage('DeploToProd') {
            when {
                allOf {
                    branch 'production'
                    environment name: 'DEPLOY_TO' , value: 'productionenv'
                }
            }
            steps {
                echo "deploying to Prod env"
            }
        }
    
    }
}
