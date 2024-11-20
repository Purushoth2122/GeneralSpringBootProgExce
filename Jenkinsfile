pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git branch: 'development', url: 'https://github.com/Purushoth2122/GeneralSpringBootProgExce.git'
                sh 'mvn clean install sonar:sonar -Dsonar.password=1234 -Dsonar.login=admin'
            }
        }
        
         stage('Test') {
            steps {
               echo "Test"
             
            }
        }
    }
}
