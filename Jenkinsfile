
pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/yourusername/RegressionTesting.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Test Report') {
            steps {
                junit '**/target/surefire-reports/*.xml'
            }
        }
    }
}
