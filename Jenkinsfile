pipeline {
    agent any

    environment {
        ARM_SUBSCRIPTION_ID = credentials('subscription_id')
        ARM_CLIENT_ID = credentials('client_id')
        ARM_CLIENT_SECRET = credentials('secret_id') 
        ARM_TENANT_ID = credentials('tenant_id')
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Terraform_AKS') {
            steps {
                sh 'terraform init'
                sh 'terraform fmt'
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
