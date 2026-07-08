pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: '<your-git-server-url>'
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'docker build -t localhost:5000/python-demo:v1 .'
                }
            }
        }

        stage('Push') {
            steps {
                script {
                    sh 'docker push localhost:5000/python-demo:v1'
                }
            }
        }
    }
}

