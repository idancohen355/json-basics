@Library('shared-library') _

pipeline {
    agent any

    stages {
        stage('Read Version') {
            steps {
                script {
                    def versionInfo = getVersion("${env.WORKSPACE}/version.json")
                    echo "Version: ${versionInfo.version}, Build: ${versionInfo.build}"

                    env.APP_VERSION = versionInfo.version
                    env.APP_BUILD = versionInfo.build.toString()
                }
            }
        }

        stage('Build') {
            steps {
                echo "Building version ${env.APP_VERSION} - build ${env.APP_BUILD}"
                // Your build steps here
            }
        }

        stage('Test') {
            steps {
                echo "Testing version ${env.APP_VERSION}"
                // Your test steps here
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying version ${env.APP_VERSION} - build ${env.APP_BUILD}"
                // Your deploy steps here
            }
        }

    }
}
