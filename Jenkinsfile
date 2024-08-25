pipeline {
    agent any
    environment {
        DIRECTORY_PATH = '/path/to/my/codefile'    
        TESTING_ENVIRONMENT = 'QA'
        PRODUCTION_ENVIRONMENT = 'Chandan'      
    }
    stages {
        stage('Build') {
            steps {
                echo "Build :Fetch the source code from the directory path specified by the environment variable: ${env.DIRECTORY_PATH}"
                echo "Build :Compile the code and generate any necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Test :Running unit tests"
                echo "Test :Running integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "code quality :Check the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy :Deploy the application to the testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                echo "approval :Waiting for manual approval"
                sleep 10 // Sleep for 10 seconds to simulate manual approval
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "production :Deploy the code to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
            }

        }
    }
}
