pipeline {
    agent any
    
    stages {
        stage('Run Python Script') {
            steps {
                // Run your Python script
                sh 'aws s3 ls' // Replace 'your_script.py' with the actual Python script filename
            }
        }
    }
}
