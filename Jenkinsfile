pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Build') {
            steps {
                echo 'This stage will build the code.'
            }
        }
        stage('Deploy') {
            steps {
                echo 'his stage will deploy the code.'
            }
        }
        stage('Test') {
            steps {
                echo 'This stage will execute the Tests'
                sh 'javac Hello.java'
                sh 'java Hello'
            }
        }
        stage('Release') {
            steps {
                echo 'Release is done successfully'
            }
        }
    }
}
