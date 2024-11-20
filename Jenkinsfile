pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                // Check out the code from the development branch
                git branch: 'development', url: 'https://github.com/Purushoth2122/GeneralSpringBootProgExce.git'
            }
        }
        stage('Build') {
            steps {
                // Run Maven clean and package commands
                sh 'mvn clean package'
            }
        }
    }
}

