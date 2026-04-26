pipeline {
    agent any

    tools {
        maven 'maven3'
    }

    stages {

        stage('CHECKOUT') {
            steps {
                git branch: 'main', url: 'https://github.com/Srushti-hidakal/c2.git'
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('demo') {
                    bat 'mvn test'
                }
            }
        }

    }
}
