pipeline {
    agent any
    stages {
        stage('testing pipeline'){
            steps {
                echo 'test1'
                sh 'mkdir -p from-jenkins'
                sh 'touch from-jenkins/test.txt'
                sh 'hostname'
                sh 'hostname -i'
                sh 'docker ps'
             }
        }
    }
}
