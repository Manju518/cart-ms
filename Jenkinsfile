pipeline{
    agent any
    environment{
        Deploy_to ='production'
    }
    stages{
        stage('DeploytoDev') {
            steps {
            echo "deploying to Dev env"
            }
        }
        stage('DeploToProd') {
            when {
                allof{
                branch 'production'
                environment name='Deploy_to' , value :'production'
                }

            }
            steps {
             echo "deploying to Prod env"
            }
        }
    
    }
}
