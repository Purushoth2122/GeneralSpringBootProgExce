pipeline {
    agent any

    tools {
        maven 'maven3' // Use the exact Maven name configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'development', url: 'https://github.com/Purushoth2122/GeneralSpringBootProgExce.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }

    post {
        always {
            echo "Pipeline execution completed!"
        }
    }
}

