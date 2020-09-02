pipeline {
    agent any
    tools {
        maven 'M2_HOME'

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('build') {
            steps {
                echo 'Hello build'
                sh 'mnv clean'
                sh 'mnv install'
                sh 'mnv package'
            }
        }
        stage('deploy') {
            steps {
                echo 'Hello deploy'
                
            }
        }
        stage('test') {
            steps {
                echo 'Hello test'
            }
        }
    }
}
