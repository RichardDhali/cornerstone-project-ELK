pipeline {
    agent any
  tools {
  terraform 'terraform'
}



    stages {
        stage('Git Checkout') {
            steps {
              git branch: 'main ', credentialsId: 'c3837a22-1b7c-4a7b-9a09-4161a415cb2c', url: 'https://github.com/RichardDhali/cornerstone-project-ELK.git'
            }
        }
        stage('Terraform init') {
            steps {
                sh 'terraform init'
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }
}

