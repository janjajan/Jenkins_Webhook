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
                build job: 'First_Jenkins_Job', parameters: [string(name: 'Tag_Name', value: '@smoke'), booleanParam(name: 'isWebTest', value: true), string(name: 'Browser', value: 'chrome')]
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
