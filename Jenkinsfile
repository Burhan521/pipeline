node {
    // Define the GitHub repository URL and credentials (if needed)
    def gitRepo = 'https://github.com/Burhan521/pipeline.git'
    def gitCredentials = 'your-git-credentials-id' // Optional

    // Checkout the code from the GitHub repository
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'CleanBeforeCheckout'], [$class: 'CloneOption', depth: 1, noTags: true, reference: '', shallow: true], [$class: 'RelativeTargetDirectory', relativeTargetDir: '']], submoduleCfg: [], userRemoteConfigs: [[credentialsId: gitCredentials, url: gitRepo]]])

    // Run the Python script
    stage('Run Python Script') {
        steps {
            sh 'python python.py' // Replace 'your_script.py' with the actual script name
        }
    }
}
