pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: 'github-ecommerce',
                    url: 'https://github.com/plsmailranjith1-awsdevops/Multi-cloud-ecommerce-devops.git'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t ecommers-app:1.0 .'
            }
        }
    }
}
