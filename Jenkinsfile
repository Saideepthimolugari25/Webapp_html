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
    }
}

