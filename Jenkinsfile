pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')   // check GitHub mỗi ~5 phút
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the code'
                echo 'Tool: Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests and integration tests'
                echo 'Tools: JUnit (unit), Selenium (integration)'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse code quality against industry standards'
                echo 'Tool: SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Task: Scan code and dependencies for vulnerabilities'
                echo 'Tool: OWASP Dependency-Check'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy application to staging server (AWS EC2)'
                echo 'Tool: AWS CodeDeploy'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests in production-like environment'
                echo 'Tool: Postman / Newman'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy application to production server (AWS EC2)'
                echo 'Tool: AWS CodeDeploy'
            }
        }
    }
}
