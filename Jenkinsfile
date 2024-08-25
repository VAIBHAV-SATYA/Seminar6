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
                echo "Building using Maven"
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Test :Running unit tests in JUNIT"
                echo "Test :Running integration tests in MOCKITO"
            }
        }
        stage('Code Analysis') {
            steps {
                echo "code quality :Check the quality of the code in SONARQUBE"
            }
        }
        stage('Security Scan') {
            steps {
                echo "conducting the security scan in ZAP"
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "deploy the application to AWS EC2 instance"
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "running the integration tests on maven to ensure the aplication functions as expected"
            }
        }
        stage('Deploy to Production') {
            steps {
                echo " deploy the application to AWWS EC2 instance"
            }
        }
    }
    post{
        success {
            emailext body: 'Jenkins exp6: success',
                subject: 'Jenkins success',
                attachLog: true,
                to: 'chandanhegde7299@gmail.com'
        }
        failure {
            emailext body: 'Jenkins exp6: failure',
                subject: 'Jenkins failure',
                attachLog: true,
                to: 'chandanhegde7299@gmail.com'
        }
    }
}
