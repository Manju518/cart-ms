pipeline{
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages{ 
        stage('ProdDeploy') {
            when 
            {
                equals expected:"Prod" actual:"${DEPLOY_TO}"
            }
            steps{
                echo "Deploy to production"
            }
        }

    }
}
