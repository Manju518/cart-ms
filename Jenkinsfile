pipeline {
    agent any
    environment {
        course= "Docker & K8s"
        name = "Manju"
    }
    stages {
        stage ('Build') {
            environment {
                cloud="GCP"
            }
            steps {
                echo "Welcome ${name}"
                echo "You enrolled for ${course}"
                echo "You are certified in ${cloud}"
            }
        }
        stage ('Secondstage') { 
            steps {
                echo "Welcome ${name}"
                echo "You enrolled for ${course}"
                echo "You are certified in ${cloud}"
            }
            
         }
    }
}
