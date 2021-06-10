pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat './gradlew.bat classes'
            }
        }

        stage('Test') {
        when {
            anyOf {
                    branch 'develop'
                    branch 'main'
                    }
                }
            steps {
                bat './gradlew.bat test'
            }
        }

        stage('Package') {
        when {
            branch 'main'
        }
            steps {
                bat './gradlew.bat jar'
            }
        }
    }
}