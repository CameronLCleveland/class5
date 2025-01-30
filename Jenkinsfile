pipeline {
    agent any  // Runs on the available node (Built-In Node in your case)

    environment {
        TF_DIR = '/path/to/your/terraform/aws/class5'  // Adjust this path for Linux
    }

    stages {
        stage('Initialize Terraform') {
            steps {
                sh "cd ${TF_DIR} && terraform init"  // Use sh instead of bat for Linux
            }
        }
        stage('Validate Terraform') {
            steps {
                sh "cd ${TF_DIR} && terraform validate"  // Use sh for Linux
            }
        }
        stage('Plan Terraform') {
            steps {
                sh "cd ${TF_DIR} && terraform plan -out=tfplan"  // Use sh for Linux
            }
        }
        stage('Apply Terraform') {
            steps {
                sh "cd ${TF_DIR} && terraform apply -auto-approve"  // Use sh for Linux
            }
        }
    }
}


