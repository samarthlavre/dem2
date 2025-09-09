pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from GitHub
                git branch: 'main', url: 'https://github.com/your-username/your-python-app.git'
            }
        }

        stage('Build with Maven') {
            steps {
                // Clean and build using Maven
                sh 'mvn clean install'
            }
        }

        stage('Run Python App') {
            steps {
                // Run the Python app after successful build
                sh 'python app.py'
            }
        }
    }
}
