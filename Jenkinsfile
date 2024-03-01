pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                 git 'https://github.com/Souvysam/jenkinsdockers.git'
                sh './mvnw compile'
                echo 'Maven Buid Successful'
            }
        }
        stage('Test') {
            steps {
              
                sh './mvnw test'
                echo 'TestCases Executed Successfully'
            }
        }
        stage('package') {
            steps {
                 sh './mvnw package'
                echo 'Application deployed Successully'
            }
        }
    }
}
