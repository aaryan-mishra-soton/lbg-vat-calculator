pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: "CHANGE ME PLEASE THANK YOU"
                }
            }
            stage('SonarQube Analysis') {
                environment {
                    scannerHome = tool 'sonarqube'
                    }
                steps {
                    withSonarQubeEnv('sonar-qube-1') {
                        sh "${scannerHome}/bin/sonar-scanner"
                        }
                }
            }
    }
}