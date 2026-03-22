pipeline {
    agent any
    tools {
        maven 'Maven_3.8.6'   // Name from Jenkins Global Tool Config
        jdk 'JDK17'           // Or whichever JDK you configured
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/pranita1991/Jenkinsfile.git'
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
    }
}
pipeline { agent any; stages { stage('Build') { steps {echo 'Hello Jenkins' } } } }
