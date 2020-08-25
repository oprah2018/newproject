pipeline {
    agent any
    tools {
       maven 'M2_HOME'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test' 
            }
        }
        stage('deploy stage') {
            steps {
                echo 'deploy stage'
                sleep 1
            }
        }
        stage('docker') {
            steps {
                echo 'image step'
                sleep 1
            }
        }
    }
}
