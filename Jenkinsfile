pipeline {
    agent any
    environment {
        JOB_URL="${JENKINS_URL}${JOB_BASE_NAME}"
        BUILD_URL="${JOB_URL}/${BUILD_NUMBER}/"
    }
    stages {
        stage('testing pipeline'){
            steps {
                echo 'test1'
                sh 'mkdir -p from-jenkins'
                sh 'touch from-jenkins/test.txt'
                sh 'hostname'
                sh 'hostname -i'
                sh 'docker ps'
                sh 'echo JENKINS_URL: ${JENKINS_URL}.'
                sh 'echo JOB_NAME: ${JOB_NAME}.'
                sh 'echo JOB_URL: ${JOB_URL}.'
                sh 'echo BUILD_ID: ${BUILD_ID}.'
                sh 'echo BUILD_NUMBER: ${BUILD_NUMBER}.'
                sh 'echo BUILD_URL: ${BUILD_URL}.'
             }
        }
    }
    post {
        success {
             echo "Test succeeded for ${env.BUILD_URL}."
        }
        failure {
             echo "Test failed for ${env.BUILD_URL}."
        }
        aborted {
             echo "Test cancelled for ${env.BUILD_URL}."
        }
    }
}
