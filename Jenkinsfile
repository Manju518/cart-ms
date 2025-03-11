pipeline{
    agent any
    stages {
        stage('Build')
        {
            steps{
                echo "Building the project"
            }
        }
        stage('Parallelstagescans') {
            parallel {
                stage ('codeanalysis')
                {
                    steps {
                        echo "Running the code analysis"
                    }
                }
                stage ('securityscan')
                {
                    steps {
                        echo "Running the security scan"
                        sleep 10
                    }
                }
                stage ('PerformanceTest')
                {
                    steps {
                        echo "Running the performance test"
                        sleep 10
                    }
                }
            }
        }
    }
}
