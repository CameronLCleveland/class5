pipeline {
    agent any  // Runs on any available Jenkins agent

    environment {
        TF_DIR = 'C:\\terraform\\aws\\class5'  // Windows file path (double backslashes)
    }

    stages {
        stage('Initialize Terraform') {
            steps {
                bat "cd %TF_DIR% && terraform init"
            }
        }
        stage('Validate Terraform') {
            steps {
                bat "cd %TF_DIR% && terraform validate"
            }
        }
        stage('Plan Terraform') {
            steps {
                bat "cd %TF_DIR% && terraform plan -out=tfplan"
            }
        }
        stage('Apply Terraform') {
            steps {
                bat "cd %TF_DIR% && terraform apply -auto-approve"
            }
        }
    }
}
