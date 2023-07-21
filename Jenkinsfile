pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://https://github.com/akash-p-07/Python-Build-Test-Procj.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://https://github.com/akash-p-07/Python-Build-Test-Procj.git'
                sh 'python3 ops.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }
    }
}
