pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git branch: 'development', url: 'https://github.com/aamirpatel/GeneralSpringBootProgExce.git'
                sh 'mvn clean install'
            }
        }
        
         stage('Test') {
            steps {
               echo "Test"
             
            }
        }
    }
}