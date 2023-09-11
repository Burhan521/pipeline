pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                script {
                    def gitURL = 'https://github.com/Burhan521/pipeline.git'
                    def gitCredentials = credentials('Burhan521') // Configure GitHub credentials in Jenkins
                    checkout([$class: 'GitSCM', branches: [[name: 'main']], userRemoteConfigs: [[url: gitURL, credentialsId: gitCredentials]]])
                }
            }
        }
        
        stage('Run Python Script') {
            steps {
                // Run your Python script
                sh 'python3 python.py' // Replace 'your_script.py' with the actual Python script filename
            }
        }
    }
}
