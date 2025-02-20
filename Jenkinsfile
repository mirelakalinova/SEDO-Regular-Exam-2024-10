pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your version control system
                git 'https://github.com/your-repo/your-project.git'
            }
        }

        stage('Build') {
            steps {
                // Add your build commands here
                // Example for a Maven project
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Add commands to run your tests
                // Example for a Maven project
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            // Actions that run regardless of build success/failure
            junit 'target/surefire-reports/*.xml' // Collect and display test results
            cleanWs() // Clean workspace after build
        }
    }
}
