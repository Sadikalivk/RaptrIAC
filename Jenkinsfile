pipeline {
    agent any

    stages {
        stage('Checkout Git') {
            steps {
               git branch: 'main', url: 'https://github.com/Sadikalivk/RaptrIAC.git'
          }
        }
        stage('Terraform init') {
            steps {
               sh 'terraform init'
          }
        }
        stage('Terraform plan') {
            steps {
               sh 'terraform plan'
          }
        }
        stage('terrform apply') {
            steps {
              sh 'terraform apply -auto-approve'
          }
        }
        
    }
}
