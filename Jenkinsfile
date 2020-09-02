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
        stage('test') {
            steps {
                sh 'mvn test'
                
            }
        }
        stage (' build and publish image')
      steps {
          script {
          checkout scm
          docker.withRegistry('', 'dockerUserID') {
              def customImage = docker.build("magloire1/hol-pipeline:${env.BUILD_ID}"}
                                             customImage.push()
                                             
                }                                
            }
        
            }
       }
