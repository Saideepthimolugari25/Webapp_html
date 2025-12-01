pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building app..."
            }
        }

        stage('Run') {
            steps {
                echo "Running app..."
            }
        }
        stage('Test') {
            steps {
                echo "Testing app..."
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '/*.index.html', fingerprint: true
            }
        }

        post{
            SUCCESS{
                echo "Pipeline completed successfully."
            }
            FAILURE{
                echo "Pipeline failed. Please check the logs."
            }
        }
    }
}
