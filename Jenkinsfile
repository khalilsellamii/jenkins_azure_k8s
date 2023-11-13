pipeline {
    agent any

    environment {
        ARM_SUBSCRIPTION_ID = '8e69d0ff-a415-4fc3-b703-78db12528a00'
        ARM_CLIENT_ID = '851de447-6854-4d84-b661-65186b807d21'
        ARM_CLIENT_SECRET = 'NRJ8Q~slEB.3PndsPILG8.FLeh3kpN9pgUr3saDm' 
        ARM_TENANT_ID = 'dbd6664d-4eb9-46eb-99d8-5c43ba153c61'
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
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
