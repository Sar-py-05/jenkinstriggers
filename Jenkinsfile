pipeline {
    agent any

    tools {
        maven 'MAVEN3'
    }

    stages {

        stage('Fetch code') {
            steps {
                git branch: 'paac', url: 'https://github.com/Sar-py-05/vprofile-project_devopshydclub.git'
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