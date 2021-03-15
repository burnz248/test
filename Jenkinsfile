pipeline {
    agent any

    stages {
        stage('Slack Started') {
            steps {
                slackSend message:"Build Started - ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)"
            }
        }
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Slack Ended') {
            steps {
                slackSend message:"Build Finished - ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)"
            }
        }
    }
}