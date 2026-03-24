pipeline {
    agent any
    tools {
        jdk 'JDK25'             // must match Jenkins tool config
        maven 'Maven_3.9.14'    // must match Jenkins tool config
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/pranita1991/Jenkinsfile.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
