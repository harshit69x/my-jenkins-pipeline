pipeline {
    agent any

    tools {
        maven 'Maven 3.8.8'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yourusername/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Test Report') {
            steps {
                junit '**/target/surefire-reports/*.xml'
            }
        }
    }
}
