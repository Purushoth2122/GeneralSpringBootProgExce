pipeline {
    agent any
    tools {
        maven 'Maven' // Refers to the Maven tool in Jenkins Global Configuration
    }
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'development', url: 'https://github.com/Purushoth2122/GeneralSpringBootProgExce.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install sonar:sonar -Dsonar.password=1234 -Dsonar.login=admin'
            }
        }
    }
}

