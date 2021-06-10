pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat './gradlew.bat classes'
            }
        }

        stage('Test') {
                    steps {
                        bat './gradlew.bat test'
            }
        }

        stage('Package') {
                    steps {
                        bat './gradlew.bat jar'
                }
            }
        }
    }