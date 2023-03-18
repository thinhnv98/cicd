pipeline {
environment {
    PATH = "$PATH:/usr/local/bin"
  }
    agent any

    stages {
        stage('Clone') {
                steps {
                    git 'https://github.com/thinhnv98/cicd'
                }
            }
        stage('Build') {
            steps {
                echo 'Building....'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing....'
            }
        }
        stage('Deploy') {
            steps {
                dir('cicd') {
                    sh '/usr/local/bin/docker-compose up -d'
                }
            }
        }
    }
}
