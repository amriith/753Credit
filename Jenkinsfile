pipeline {
    agent any
    
    stages {
        stage("Build") {
            steps {
                echo "Building..."
                echo "Build automation tool: Maven"
            }
        }

        stage("Unit and Integration Test") {
            steps {
                echo "Running tests..."
                echo "Test automation tool: Selenium"
            }
            post {
                success {
                    mail to: "appureejajayadeep@gmail.com",
                    subject: "Unit and Integration Test Status",
                    body: "Unit and Integration tests were successful!",
                    attachLog: true
                }
            }
        }

        stage("Code Analysis") {
            steps {
                echo "Analyzing code..."
                echo "Code analysis tool: SonarQube"
            }
        }

        stage("Security Scan") {
            steps {
                echo "Performing security scan..."
                echo "Security scan tool: Checkmarx"
            }
            post {
                success {
                    mail to: "appureejajayadeep@gmail.com",
                    subject: "Security Scan Status",
                    body: "Security scan was successful!",
                    attachLog: true
                }
            }
        }

        stage("Integration Tests on Staging") {
            steps {
                echo "Testing on staging environment..."
            }
        }

        stage("Deploy") {
            steps {
                echo "Deploying..."
                echo "Production server: AWS EC2"
            }
        }
    }
}
