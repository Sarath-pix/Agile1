pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Sarath-venkat/Jenkins1.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Run Unit Tests') {
            steps {
                sh 'python3 -m pytest test_app.py'
            }
        }
    }
}