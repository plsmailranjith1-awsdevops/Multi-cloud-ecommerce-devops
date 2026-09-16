pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: '61660147-ff0c-4d17-89ca-af294d249c9e',
                    url: 'https://github.com/plsmailranjith1-awsdevops/Multi-cloud-ecommerce-devops.git'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t ecommers-app:1.0 .'
            }
        }

        stage('Docker Run') {
            steps {
                sh 'docker rm -f ecommerce-app || true'
                sh 'docker run -d --name ecommerce-app -p 5000:5000 ecommers-app:1.0'
            }
        }
    }
}
