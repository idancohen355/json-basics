@Library('shared-library') _

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building"
                // Your build steps here
            }
        }

        stage('Test') {
            steps {
                echo "Testing"
                // Your test steps here
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying"
                // Your deploy steps here
            }
        }

        stage('Read JSON') {
            steps {
                script {
                    def jsonFilePath = 'sample.json'  // Make sure this path is correct
                    def jsonString = readJsonFile(jsonFilePath)
                    echo "JSON Content as String: ${jsonString}"
                }
            }
        }
    }
}
