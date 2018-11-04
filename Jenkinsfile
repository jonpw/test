pipeline {
    agent none
    stages {
        stage('Back-end') {
            agent { dockerfile true }
            steps {
                checkout scm
                sh 'cat README.md'
            }
        }
        stage('Front-end') {
            agent {
                docker { image 'debian/latest' }
            }
            steps {
                sh 'cat LICENSE'
            }
        }
    }
}