pipeline {
    agent any

    tools {
        // Set up tools as per your Jenkins configurations
        jdk 'JDK11'
        maven 'Maven3'
    }

    stages {
        stage('Checkout') {
            steps {
                // Clone the specific branch
                git branch: 'development', url: 'https://github.com/Purushoth2122/General-SpringBootProgExce.git'
            }
        }

        stage('Build') {
            steps {
                // Clean and package using Maven
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Run tests using Maven
                sh 'mvn test'
            }
        }

        stage('Archive') {
            steps {
                // Archive JAR/WAR files generated
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }

    post {
        always {
            // Actions to perform after pipeline completes
            echo "Pipeline execution completed!"
        }
    }
}

