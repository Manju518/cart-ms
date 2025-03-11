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
                name="Ram"
            }
            steps {
                echo "Welcome ${name}"
                echo "You enrolled for ${course}"
                echo "You are certified in ${cloud}"
                echo "My branch is ${env.BRANCH_NAME}"
            }
        }
    }
}
