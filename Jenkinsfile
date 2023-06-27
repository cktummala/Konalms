pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "building"
            }
        }

         stage('Send Slack Notification') {
            steps {
                script {
                    slackSend channel: 'jenkinsnotification',
                              color: 'good',
                              message: 'Welcome jenkins',
                              tokenCredentialId: 'c6aa68a8-71a7-46a5-8fce-a2b79cd7f706'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo "deploying"
            }
        }
    }
}
